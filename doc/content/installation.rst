===========================================================
ScaleIO Cinder plugin installation
===========================================================
The first step is to install the ScaleIO Cinder plugin in the Fuel Master:

1. Download the plugin from the https://github.com/openstack/fuel-plugin-scaleio-cinder/releases "Releases Page" or from the https://www.mirantis.com/products/openstack-drivers-and-plugins/fuel-plugins/ "Fuel Plugins Catalog".
 
2. Copy the plugin to an already installed Fuel Master node. If you do not have the Fuel Master node yet, follow the instructions from the official Mirantis OpenStack documentation:

     `scp  fuel-plugin-scaleio-cinder-1.0.noarch.rpm root@:<the_Fuel_Master_node_IP>:/tmp`

3. Log into the Fuel Master node and install the plugin, if downloaded in the `/tmp` directory:

	`cd /tmp`
	`fuel plugins --install /tmp/fuel-plugin-scaleio-cinder-1.0.noarch.rpm`
    

4. Verify that the plugin has been installed successfully: 

.. image:: https://github.com/openstack/fuel-plugin-scaleio-cinder/blob/master/doc/images/scaleio-cinder-install-1.png


===========================================================
ScaleIO Cinder plugin configuration
===========================================================
Once the plugin has been installed in the Master, we configure the nodes and set the parameters for the plugin:


1. Start by creating a new OpenStack environment following the https://docs.mirantis.com/openstack/fuel/fuel-6.1/user-guide.html#create-a-new-openstack-environment "Creating a new OpenStack environment") 

2. Configure your environment following the https://docs.mirantis.com/openstack/fuel/fuel-6.1/user-guide.html#configure-your-environment

	.. image:: https://github.com/openstack/fuel-plugin-scaleio-cinder/blob/master/doc/images/scaleio-cinder-install-2.png

3. Open the **Settings tab** of the Fuel web UI and scroll down the page. Select the Fuel plugin check-box to enable ScaleIO Cinder plugin for Fuel:

	.. image:: https://github.com/openstack/fuel-plugin-scaleio-cinder/blob/master/doc/images/scaleio-cinder-install-4.PNG
	
	**Plugin's parameters explanation:** 
	
	+-------------------------+---------------------------------------------------------+
	|Parameter Name           |Parameter Description				    |
	+=========================+=========================================================+
	|userName                 |The ScaleIO User Name				    |
	+-------------------------+---------------------------------------------------------+
	|Password                 |The SclaeIO password for the selected user name	    |
	+-------------------------+---------------------------------------------------------+
	|ScaleIO GW IP            |The IP address of the the ScaleIO Gateway service	    |
	+-------------------------+---------------------------------------------------------+
	|ScaleIO Primary IP       |The ScaleIO cluster's primary IP address		    |
	+-------------------------+---------------------------------------------------------+
	|ScaleIO Secondary IP     |The ScaleIO cluster's secondary IP address		    |
	+-------------------------+---------------------------------------------------------+
	|ScaleIO protection domain|Name of the ScaleIO's protection domain		    |
	+-------------------------+---------------------------------------------------------+
	|ScaleIO storage pool 1   |Name of the first storage pool			    |
	+-------------------------+---------------------------------------------------------+
	
	**Note:** Please refer to the ScaleIO documentation for more information on these parameters 

	This is an example of the ScaleIO configuration paremets populated: 

	.. image:: https://github.com/openstack/fuel-plugin-scaleio-cinder/blob/master/doc/images/scaleio-cinder-install-5.PNG

4. After the configuration is done, you can Add the nodes to the Openstack Deployment. 
	.. image:: https://github.com/openstack/fuel-plugin-scaleio-cinder/blob/master/doc/images/scaleio-cinder-install-3.PNG

**Note:** you can run the 
check and https://docs.mirantis.com/openstack/fuel/fuel-6.1/user-guide.html#deploy-changes. 

After this is complete you should see a success message:
	.. image:: https://github.com/openstack/fuel-plugin-scaleio-cinder/blob/master/doc/images/scaleio-cinder-install-complete.jpg

**Note:** It make take an hour or more for the OpenStack deployment to complete, depending on your hardware configuration. 

