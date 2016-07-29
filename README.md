# Create RPM for Tomcat 8
Tomcat8 RPM for RHEL/Centos

# How to build

  - yum -y install rpmdevtools
  - Copy files to their respective folders (SPECS and SOURCES)
  - Run the following command:
    rpmbuild -ba ~/rpmbuild/SPECS/tomcat8.spec
  - Once finished, check ~/rpmbuild/RPMS/noarch/ for your file (should be called tomcat8-8.0.21-1.noarch.rpm).

# .SPEC config

    - Store configs on /etc/tomcat8 (symlink)
    - Logs on /var/log/tomcat8 (symlink)
    - Logrotate on /etc/logrotate.d
    - CATALINA_HOME on /usr/share/tomcat8
    - Creates user:group tomcat8
    - Permissions for that user to own and run tomcat8 files
    
