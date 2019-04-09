# Check SVN Repositores

It's a simple bash script that supposed to check repository status and trigger an exit code accordingly.

# Usage
check_svn_repo.sh *SERVER_ADDRESS* *REPO_NAMES*

Just replace *SERVER_ADDRESS* and *REPO_NAMES* with your server.

# Required parameters

1. You have to add your SVN user name and password, otherwise it won't work.
Just modify the code and look for these lines:

**USER=XXX #user name here**

**PASS=XXX #password here**

Replace *XXX* with your credentials.

2. You have to provide a minimum one repositry name to check. 
If you want to add several repositories, you have to use the '#' delimiter, for example:

**repo_name1#reponame_2#repo_name3**

# Exit codes
The exit codes are basic:
- 0 = OK
- 1 = WARNING
- 2 = CRITICAL
- 3 = UNKNOWN

# Where can you use it?
You can use it as a stand alone script or you can use it for monitoring systems such as Nagios, Sensu etc.

