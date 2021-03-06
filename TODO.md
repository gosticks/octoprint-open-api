# TODO

## General

- [ ] handle authorization header
- [ ] update readme

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
- [x] Languages [link](https://docs.octoprint.org/en/master/api/languages.html)
  - [x] Retrieve installed language packs
  - [x] Upload a language pack
  - [x] Delete a language pack
  - [x] Model: List response
  - [x] Model: Component list
  - [x] Model: Language pack metadata
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
- [x] Printer profile operations [link](https://docs.octoprint.org/en/master/api/printerprofiles.html)
  - [x] Retrieve all printer profiles
  - [x] Retrieve a single printer profile
  - [x] Add a new printer profile
  - [x] Update an existing printer profile
  - [x] Remove an existing printer profile
  - [x] Model: Profile list
  - [x] Model: Add or update request
  - [x] Model: Profile
- [x] Settings [link](https://docs.octoprint.org/en/master/api/settings.html)
  - [x] Retrieve current settings
  - [x] Save settings
  - [x] Regenerate the system wide API key
  - [x] Fetch template data
  - [ ] Model: Config
- [ ] Slicing TBD [link](https://docs.octoprint.org/en/master/api/slicing.html)
- [x] System [link](https://docs.octoprint.org/en/master/api/system.html)
  - [x] List all registered system commands
  - [x] List all registered system commands for a source
  - [x] Execute a registed system command
  - [x] Model: List all response
  - [x] Model: Client command definitions
  - [x] Model: Command definition
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
- [x] Access Control [link](https://docs.octoprint.org/en/master/api/access.html)
  - [x] List all permissions
  
  Groups

  - [x] Get group list
  - [x] Add a new group
  - [x] Retrieve a group
  - [x] Update a group
  - [x] Delete a group
  
  Users
  
  - [x] Retrieve list of users
  - [x] Retrieve user
  - [x] Add new user
  - [x] Update user
  - [x] Delete user
  - [x] Change users password
  - [x] Get a users password
  - [x] Update users password
  - [x] Update users settings
  - [x] Regenerate users api key
  - [x] Delete users api key
  - [x] Model: Permission list response
  - [x] Model: Group list response
  - [x] Model: Group registration request
  - [x] Model: Group update request
  - [x] Model: User list response
  - [x] Model: User registration request
  - [x] Model: User update request
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
