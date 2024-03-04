# Configure-Azure-Virtual-Networking

In this project, you will control virtual network traffic. First, you will create a virtual network. Next, you will implement Azure virtual network routing. 
Finally, you will implement network security groups and application security groups.

#__Creating a virtual network__

Create an Azure virtual network (VNet) by using the values in the following table:

__Resource group__:	AZ300-RGlod38474410 </br>
__Name__:	NewVNet </br>
__Region__: East US 2</br>
__IPv4 address space__:	10.1.0.0/16</br>
__Subnet name__:	Production</br>
__Subnet address range__:	10.1.0.0/24</br>

![img1](https://github.com/mbahl1990/Configure-Azure-Virtual-Networking/assets/161914219/f5ffb9ae-9308-4700-a4e8-7409183fe3e8)


#__Creating a Route table__


Create a route table named RouteTablePublic that uses the AZ300-RGlod38474410 resource group and the (US) East US 2 region. </br>

Add a route named ToPrivateSubnet to the RouteTablePublic route table, and then configure the route by using an address prefix of 10.0.1.0/24 and a virtual appliance next hop address of 10.0.2.4. </br>

Associate the RouteTablePublic route table to the Public subnet in the MyVNet VNet. </br>

![img2](https://github.com/mbahl1990/Configure-Azure-Virtual-Networking/assets/161914219/45ee9615-c006-418e-b40c-302fbd1d8b57)

#__Creating Application Security Groups__

Create an application security group named ASG-WebServers that uses the AZ300-RGlod38474410 resource group and the (US) East US 2 region.</br>

Create an application security group named ASG-MgmtServers that uses the AZ300-RGlod38474410 resource group and the (US) East US 2 region. </br>

![img1](https://github.com/mbahl1990/Configure-Azure-Virtual-Networking/assets/161914219/e4dd0365-7e4c-4e7c-95ad-e8a0405d95e3)

#__Creating Network Security Groups__

Create a network security group named MyNSG that uses the AZ300-RGlod38474410 and the (US) East US 2 region. </br>

Associate the MyNSG network security group to the Public subnet in the MyVNet VNet.


![img2](https://github.com/mbahl1990/Configure-Azure-Virtual-Networking/assets/161914219/3f6ac3f1-049a-4b13-b766-7250ff1c0c7e)

![img1](https://github.com/mbahl1990/Configure-Azure-Virtual-Networking/assets/161914219/2b95aac6-8284-4b9a-aff4-0c82f8344bca)

#__Create security rules__

Create an inbound security rule named Allow-Web-All in the MyNSG network security group, and then configure the rule to allow incoming TCP traffic on ports 80 and 443 to reach the ASG-WebServers application security group.

Create an inbound security rule named Allow-RDP-All in the MyNSG network security group, and then configure the rule to allow incoming TCP traffic on port 3389 to reach the ASG-MgmtServers application security group.

![img1](https://github.com/mbahl1990/Configure-Azure-Virtual-Networking/assets/161914219/a0f54eba-d175-4a48-a73b-600e7ff8ee51)







