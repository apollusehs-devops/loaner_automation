# Loaner Self Service
## Purpose
* Create a GUI based tool which will allow users to check out loaners without the need of IT

* Allows the user to:
	* Create their own user account
* Script creates:
	* New user account via the user with GUI
	* Creates a local account on the loaner machine with credentials provided by user
	* Automates the re-provisioning of the machine for the next user


### Dependencies:
* Python 3.7 installed
* Python .env and .env credentials
	* `sudo pip3 install -U python-dotenv`

### Usage:
* Clone repo, i.e., `git clone https://github.com/aharshbe/loaner_automation`
* In your terminal, cd into the repo
* cd into `loaner_automation/files`
* Type `python3 ./loaner_automation_ui.py`

### Mongo Server initialization:
* `use <db name>`
* `db.createUser({ user: “<username>” , pwd: “<password>“,  roles: [ { role: “readWrite”, db: “<db name>“}])`
* `make .env`
  * cat .env ->
```
DB=<dbname>
USERNAME=<username>
PASSWORD=<password>
MONGOOSE_URI=mongodb://localhost:27017/
```

#### Authors:
* [Travis Kopp](https://github.com/teakopp)
* [Austin Harshberger](https://github.com/aharshbe)
