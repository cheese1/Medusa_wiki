The following instructions are for installing SickRage on CentOS 6.

The installation should also be applicable to RHEL 6 and Fedora (12, 13, or 14) with minimal changes.

The installation assumes that you're not using the root user to install/run sickrage - the entries for **user:group** throughout the document will have to be modified to match your user configuration.

1. Install rpmFusion non-free repository 
    The repository is needed for unrar installation

   ```bash
   sudo rpm -ivh http://download1.rpmfusion.org/nonfree/el/updates/6/i386/rpmfusion-nonfree-release-6-1.noarch.rpm
   ```

2. Install prerequisites

   ```bash
    sudo yum install python-cheetah unrar wget git 
    ```

3. Clone sickrage git repo

    ```bash
    sudo git clone https://github.com/echel0n/SickRage.git /usr/share/sickrage
    ```

4. Set correct ownership

    ```bash
    chown -R user:group /usr/share/sickrage
    ```

5. Copy init file to system init

    ```bash
    sudo cp /usr/share/sickrage/init.fedora /etc/init.d/sickrage
    ```

6. Make init file executable

    ```bash
    sudo chmod +x /etc/init.d/sickrage
    ```

7. Modify init file

    ```bash
    sudo sed 's|/etc/sysconfig/sickbeard|/etc/sysconfig/sickrage|' -i /etc/init.d/sickrage
    ```

8. Create configuration file /etc/sysconfig/sickrage with the following content

    ```bash
    # SickRage service configuration
    
    #run Sickbeard as
    SB_USER=media
    SB_HOME=/usr/share/sickrage
    SB_DATA=/usr/share/sickrage
    SB_PIDFILE=/usr/share/sickrage/sickrage.pid
    
    #gui address, eg: \${protocol}://\${host}:\${port}/sickrage/
    protocol=http
    host='<<< hostname or IP >>>' #example host=mymachine
    port='<<<Desired Port>>>'     #example port=8081
    
    #leave blank if no username/password is required to access the gui
    username=
    password=
    
    #use nice, ionice, taskset to start SickRage
    nicecmd=
    #  example: nicecmd="nice -n 19 ionice -c3"
    ```

9. Add the sickbeard service to system services
    
    ```bash
    sudo chkconfig --add sickrage
    ```

10. Configure sickrage service to start on system startup
    
    ```bash
    sudo chkconfig sickrage on
    ```

11. Start sickrage service
    
    ```bash
    sudo service sickrage start
    ```

All done, verify that SickRage is accessible at gui address, eg: http://mymachine:8080/sickrage

Celebrate with some impromptu dancing!!