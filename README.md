# RTL8111-RTL8168-RTL8148-wifi-driver
For wifi driver
#Installation instruction

You can find <> using lspci | grep Wireless. Afterwards, execute the following lines of codes in your shell:

You will need to install "make", "gcc", "kernel headers", "kernel build essentials", and "git".

If you are running Ubuntu, then

 sudo apt-get install linux-headers-generic build-essential git
 
 #  git clone https://github.com/deshpandeshivam23/RTL8111-RTL8168-RTL8148-wifi-driver.git
 # cd RTL8111-RTL8168-RTL8148-wifi-driver-master/
 # cd rtlwifi_new-master/
 # sudo make install 
 # modprobe rtl8723de ant_sel=1
 # modprobe rtl8723de ant_sel=1
 # vi /etc/modprobe.d/rtl8723de.conf
       options rtl8723de ant_sel=1    #( to add this line in conf file)
  # init 6
  
  
  For all distros:
 # git clone https://github.com/deshpandeshivam23/RTL8111-RTL8168-RTL8148-wifi-driver.git
 # cd RTL8111-RTL8168-RTL8148-wifi-driver-master/
 # cd rtlwifi_new-master
 # sudo make install
 # sudo modprobe -r <<YOUR WIRELESS DRIVER CODE>>
 # sudo modprobe <<YOUR WIRELESS DRIVER CODE>>

#### Option configuration
If it turns out that your system needs one of the configuration options, then do the following:

vim /etc/modprobe.d/<<YOUR WIRELESS DRIVER CODE>>.conf 

There, enter the line below:
`options <<YOUR WIRELESS DRIVER CODE>> <<driver_option_name>>=<value>`

