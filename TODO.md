# TODO

## General

- [ ] handle authorization header

## Routes

- [x] Login
- [x] Logout
- [x] Current User
- [x] Version
- [x] Connection Handling
- [x] File Operations [link](https://docs.octoprint.org/en/master/api/files.html)
  - [x] Retrieve all files
  - [x] Retrieve files from specific location
  - [x] Upload file or create folder
  - [x] Retrieve a specific file’s or folder’s information
  - [x] Issue a file command
  - [x] Delete file
  - [x] Model: Upload response
  - [x] Model: Retrieve response
- [x] Job operations [link](https://docs.octoprint.org/en/master/api/job.html)
  - [x] Issue a job command
  - [x] Retrieve information about the current job
  - [x] Model: Job information response
- [ ] Languages [link](https://docs.octoprint.org/en/master/api/languages.html)
  - [ ] Retrieve installed language packs
  - [ ] Upload a language pack
  - [ ] Delete a language pack
  - [ ] Model: List response
  - [ ] Model: Component list
  - [ ] Model: Language pack metadata
- [ ] Log file management (Plugin?) [link](https://docs.octoprint.org/en/master/bundledplugins/logging.html#sec-bundledplugins-logging-api)
  - [ ] Retrieve a list of available log files
  - [ ] Delete a specific logfile
  - [ ] Model: Logfile Retrieve Response
  - [ ] Model: File information
  - [ ] Model: References
- [x] Printer operations [link](https://docs.octoprint.org/en/master/api/printer.html)
  - [x] Retrieve the current printer state
  - [x] Issue a print head command
  - [x] Issue a tool command
  - [x] Retrieve the current tool state
  - [x] Issue a bed command
  - [x] Retrieve the current bed state
  - [x] Issue a chamber command
  - [x] Retrieve the current chamber state
  - [x] Issue an SD command
  - [x] Retrieve the current SD state
  - [x] Send an arbitrary command to the printer
  - [x] Retrieve custom controls (PARTIAL)
  - [x] Model: Full State Response
  - [x] Model: Temperature State
  - [x] Model: SD State
  - [x] Model: Arbitrary Command Request
- [ ] Printer profile operations [link](https://docs.octoprint.org/en/master/api/printerprofiles.html)
  - [x] Retrieve all printer profiles
  - [x] Retrieve a single printer profile
  - [ ] Add a new printer profile
  - [ ] Update an existing printer profile
  - [ ] Remove an existing printer profile
  - [ ] Model: Profile list
  - [ ] Model: Add or update request
  - [x] Model: Profile
- [ ] Settings [link](https://docs.octoprint.org/en/master/api/settings.html)
  - [ ] Retrieve current settings
  - [ ] Save settings
  - [ ] Regenerate the system wide API key
  - [ ] Fetch template data
  - [ ] Model: Config
- [ ] Slicing TBD [link](https://docs.octoprint.org/en/master/api/slicing.html)
- [ ] System [link](https://docs.octoprint.org/en/master/api/system.html)
  - [ ] List all registered system commands
  - [ ] List all registered system commands for a source
  - [ ] Execute a registed system command
  - [ ] Model: List all response
  - [ ] Model: Client command definitions
  - [ ] Model: Command definition
- [ ] Timelapse [link](https://docs.octoprint.org/en/master/api/timelapse.html)
  - [ ] Retrieve a list of timelapses and the current config
  - [ ] Delete a timelapse
  - [ ] Issue a command for an unrendered timelapse
  - [ ] Delete an unrendered timelapse
  - [ ] Change current timelapse config
  - [ ] Model: Timelapse list
  - [ ] Model: Rendered timelapse
  - [ ] Model: Unrendered timelapse
  - [ ] Model: Timelapse configuration
  - [ ] Model: Z-change-triggered timelapse
  - [ ] Model: Time triggered timelapse
- [ ] Access Control [link](https://docs.octoprint.org/en/master/api/access.html)
  - [ ] List all permissions
  
  Groups

  - [ ] Get group list
  - [ ] Add a new group
  - [ ] Retrieve a group
  - [ ] Update a group
  - [ ] Delete a group
  
  Users
  
  - [ ] Retrieve list of users
  - [ ] Retrieve user
  - [ ] Add new user
  - [ ] Update user
  - [ ] Delete user
  - [ ] Change users password
  - [ ] Get a users password
  - [ ] Update users password
  - [ ] Update users settings
  - [ ] Regenerate users api key
  - [ ] Delete users api key
  - [ ] Model: Permission list response
  - [ ] Model: Group list response
  - [ ] Model: Group registration request
  - [ ] Model: Group update request
  - [ ] Model: User list response
  - [ ] Model: User registration request
  - [ ] Model: User update request
- [ ] Util [link](https://docs.octoprint.org/en/master/api/util.html)
  - [ ] Test paths or URLs
  - [ ] Model: Path test result
  - [ ] Model: URL test result
  - [ ] Server test result
  - [ ] Resolution test result
- [ ] Wizard [link](https://docs.octoprint.org/en/master/api/wizard.html)
  - [ ] Retrieve additional data about registered wizards
  - [ ] Finish wizards
  - [ ] Model: Wizard data entry
- [ ] Common Data models [link](https://docs.octoprint.org/en/master/api/datamodel.html)

## LATER

- [ ] Model: Custom Controls Response
- [ ] Retrieve custom controls (FULL)
