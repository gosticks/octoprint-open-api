
# OctoPrint OpenAPI Definition (BETA!!!)

This project proved a unofficial OpenAPI specification for the popular open source 3D printer control software OctoPrint. The definitions are based on the currently available OctoPrint api documentation. 

## Working on your OpenAPI Definition

### Install

1. Install [Node JS](https://nodejs.org/).
2. Clone this repo and run `yarn install`/`npm install` in the repo root.

### Usage

#### `npm start`
Starts the reference docs preview server.

#### `npm run build`
Bundles the definition to the dist folder.

#### `npm test`
Validates the definition.

## Contribution Guide

Below is a sample contribution guide. The tools
in the repository don't restrict you to any
specific structure. Adjust the contribution guide
to match your own structure. However, if you
don't have a structure in mind, this is a
good place to start.

Update this contribution guide if you
adjust the file/folder organization.

The `.redocly.yaml` controls settings for various
tools including the lint tool and the reference
docs engine.  Open it to find examples and
[read the docs](https://redoc.ly/docs/cli/configuration/)
for more information.

### Schemas

#### Adding Schemas

1. Navigate to the `openapi/components/schemas` folder.
2. Add a file named as you wish to name the schema.
3. Define the schema.
4. Refer to the schema using the `$ref` (see example below).

##### Using the `$ref`

Notice in the complex example above the schema definition itself has `$ref` links to other schemas defined.

Here is a small excerpt with an example:

```yaml
defaultPaymentInstrument:
  $ref: ./PaymentInstrument.yaml
```

The value of the `$ref` is the path to the other schema definition.

You may use `$ref`s to compose schema from other existing schema to avoid duplication.

You will use `$ref`s to reference schema from your path definitions.

#### Editing Schemas

1. Navigate to the `openapi/components/schemas` folder.
2. Open the file you wish to edit.
3. Edit.

### Paths

#### Adding a Path

1. Navigate to the `openapi/paths` folder.
2. Add a new YAML file named like your URL endpoint except replacing `/` with `@` and putting path parameters into curly braces like `{example}`.
3. Add the path and a ref to it inside of your `openapi.yaml` file inside of the `openapi` folder.

Example addition to the `openapi.yaml` file:
```yaml
'/customers/{id}':
  $ref: './paths/customers@{id}.yaml'
```

Here is an example of a YAML file named `customers@{id}.yaml` in the `paths` folder:

```yaml
get:
  tags:
    - Customers
  summary: Retrieve a list of customers
  operationId: GetCustomerCollection
  description: |
    You can have a markdown description here.
  parameters:
    - $ref: ../components/parameters/collectionLimit.yaml
    - $ref: ../components/parameters/collectionOffset.yaml
    - $ref: ../components/parameters/collectionFilter.yaml
    - $ref: ../components/parameters/collectionQuery.yaml
    - $ref: ../components/parameters/collectionExpand.yaml
    - $ref: ../components/parameters/collectionFields.yaml
  responses:
    '200':
      description: A list of Customers was retrieved successfully
      headers:
        Rate-Limit-Limit:
          $ref: ../components/headers/Rate-Limit-Limit.yaml
        Rate-Limit-Remaining:
          $ref: ../components/headers/Rate-Limit-Remaining.yaml
        Rate-Limit-Reset:
          $ref: ../components/headers/Rate-Limit-Reset.yaml
        Pagination-Total:
          $ref: ../components/headers/Pagination-Total.yaml
        Pagination-Limit:
          $ref: ../components/headers/Pagination-Limit.yaml
        Pagination-Offset:
          $ref: ../components/headers/Pagination-Offset.yaml
      content:
        application/json:
          schema:
            type: array
            items:
              $ref: ../components/schemas/Customer.yaml
        text/csv:
          schema:
            type: array
            items:
              $ref: ../components/schemas/Customer.yaml
    '401':
      $ref: ../components/responses/AccessForbidden.yaml
  x-code-samples:
    - lang: PHP
      source:
        $ref: ../code_samples/PHP/customers/get.php
post:
  tags:
    - Customers
  summary: Create a customer (without an ID)
  operationId: PostCustomer
  description: Another markdown description here.
  requestBody:
    $ref: ../components/requestBodies/Customer.yaml
  responses:
    '201':
      $ref: ../components/responses/Customer.yaml
    '401':
      $ref: ../components/responses/AccessForbidden.yaml
    '409':
      $ref: ../components/responses/Conflict.yaml
    '422':
      $ref: ../components/responses/InvalidDataError.yaml
  x-code-samples:
    - lang: PHP
      source:
        $ref: ../code_samples/PHP/customers/post.php
```

You'll see extensive usage of `$ref`s in this example to different types of components including schemas.

You'll also notice `$ref`s to code samples.

