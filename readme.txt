curlie ---  Web based front end for snort.
feedback and bug reports to :
  K. Balasubramanian ( balu )
  balu1729@yahoo.com

Reads data from a mysql database that is fed by snort sensors.  Database
  populated by barnyard2 running on the sensors.  Displays data in
  summary form with links to more detailed information.  Alerts are
  summarized by signature and by source ( ip ).  ICMP destination
  unreachable ( host unreachable and port unreachable ) messages are
  traced back to the original datagram causing the message and displayed
  as summaries and in detail in multiple frames.

The underlying pages are updated every thirty minutes ( cron ) by pulling
  incremental data from the database.  The data for each complete day
  is also stored in archive directories and are accessible through web
  interfaces.

Requirements for package installation :
  A linux server with web server configured and running,  mysql client,
  and perl.  The package has been well tested on a Redhat ( Fedora 10 )
  installation running apache web server with Selinux enabled in 
  enforcing mode.
  It has also been tested on a Debian installation.
  It should work under other distros,  but the installation script
  will likely need tweaking.

Checklist of required information for installation :
  1. Linux server as above.
  2. Root access to the server on which the package is to be installed.
  3. Access to the database --- ( location of the database, username and
     password with read ( SELECT ) access to the snort tables ).

Package installation :
  1. Extract the files from the tar archive, preferably in an empty directory.
  2. cd to the directory the files were extracted to ( sfepkg relative
     to current )
  3. ./install
     and provide answers to questions. 

After the installation :
  use a browser to view http://linux_server/curlie   and follow the links.

Acknowledgements :
  The author acknowledges the feedback and support of coworkers --- 
  It is gratifying to see it being used to provide useful and actionable
  information ... It is hoped that others would find it useful.
