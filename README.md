# Linux Server Configuration

This project takes an installation of a Linux server (Amazon Lightsail) and hosts the Item Catalog web application I created in my previous project.  The server is also secured from attacks with firewall and limited open ports.  Finally, there is also PostgreSQL installed and configured.

### IP address and SSH port to server
* Public: `18.218.52.109`
* Private: `172.26.11.202`

### Complete URL to Item Catalog web application
* http://18.218.52.109

### Summary of software installed and configuration changes made
1.  Started a new Ubuntu Linux server instance on Amazon Lightsail and made sure TCP 2200 Port was open.
2.  Updated all currently installed packages.
3.  Change the SSH port from 22 to 2200.
4.  Configured UFW to only allow incoming connections for SSH (port 2200), HTTP (port 80), and NTP (port 123).
5.  Create a new user account named `grader` and gave permission to sudo.
6.  Create an SSH key pair for grader using the ssh-keygen tool.
7.  Configure server the local timezone to UTC.
8.  Installed and configure Apache to serve a Python mod_wsgi application.
9.  Installed and configure PostgreSQL and not to allow remote connections.
10. Created a new database user named `catalog` that has limited permissions to catalog application database.
11. Installed `git`.
12. Clone and setup your Item Catalog project from the Github repository created earlier in this program.
13. Set up in server so that it functions correctly when visiting server’s IP address in a browser.
14. `.git` directory is not publicly accessible via a browser

### A list of any third-party resources you made use of to complete this project
I used Udacity's forum mostly to get this project working.  These are the links that helped me the most:
   * https://discussions.udacity.com/t/running-my-project-on-the-linux-server/231383/22
   * https://discussions.udacity.com/t/problems-running-python-script/527370/7
   * https://discussions.udacity.com/t/no-module-name-classic-error/314342
   * https://discussions.udacity.com/t/sqlite3-operationalerror-unable-to-open-database-file-on-postgres-engine/157818
   
### Personal GitHub link for Item Catalog
* https://github.com/BenjaminGHo/catalog
* **Note**: Item Catalog displays the items and user can click around.  The authorization piece for logging into Google or Facebook's account doesn't work though.