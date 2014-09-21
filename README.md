script_inicio_servicio
======================

Script para poner cualquier servicio al inicio de Linux


Luego de crear el script:

Now you can save and close the editor. The next step is to make the script executable:

sudo chmod 755 /etc/init.d/nombredelproceso

Before to proceed any further test if the script works as expected. Try to connect to the VPN using the following command:

sudo /etc/init.d/VPNConnection start

and then test the stop command (disconnect from the VPN):

sudo /etc/init.d/nombredelproceso stop

The final step is to register the script to be run at boot and shutdown:

sudo update-rc.d nombredelproceso defaults

Next time you will boot the system you will be automatically connect to the VPN.

If you want to remove the script from the start-up:

sudo update-rc.d -f  nombredelproceso remove

Let me know if you have any comments or suggestion!
