# Change Log

## 1.5.0
* Accept job and workflow descriptions in YAML format. These are converted to JSON before being POSTed to the REST API. YAML format makes it simpler to specify commands without having to worry about escaping characters.
* If input files in job descriptions are in the form of a list of names beginning with `file://`, the specified files will be read and the content automatically added to the job description. This results in much simpler and clearer job description files.
* If a `cmd` contains multiple lines, the task will be split automatically into multiple tasks with one cmd per task. However, if the first line begins with a shebang, an input file will be created automatically and the task will execute this input file. This functionality is particularly helpful for job descriptions in the YAML format.
* Update default URL of EOSC PROMINENCE service
* Support reading token stored as a string in `~./prominence/token`
* Return an error if permissions of the token file are too open

## 1.4.0
* Changed default URL of EOSC PROMINENCE service

## 1.3.0
* Support listing jobs associated with a workflow

## 1.2.0
* Report CPU type information for completed jobs

## 1.1.0
* Support reading token from PROMINENCE_TOKEN environment variable
* Fix bug when creating jobs, introduced in 1.0.3

## 1.0.3
* Removed options when creating jobs which are not applicable

## 1.0.2
* No longer use a deprecated parameter in `jwt.decode`

## 1.0.0
* First public release
