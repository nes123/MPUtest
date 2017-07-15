    # Reach IMU data

    Download that zip, scp it over to your reach with "scp MPUtest-master.zip root@YOUR.REACH.IP.HERE:/home/root"
    SSH to the reach as user root with password emlidreach
    Unzip the file and cd into the directory
    make
    sudo ./MPUtest
    
    # bluetooth connection between edison and jetson
    
    on jetson :
    sudo rfkill unblock bluetooth
    also allow bluetooth in the settings (use GUI)
    
    on edison :
    rfkill unblock bluetooth
    bluetoothctl
    scan on
    (identify jetson address)
    scan off
    
    pair xx:xx:xx:xx:xx:xx (x's for the jetson address)
