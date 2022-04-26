

# basic-image:  registry.access.redhat.com/ubi8/ubi:8.4




OPENSHIFT EX280 
===============




Manage users and policies
-------------------------
1. identity managment 

  - add the following users with there passwords: 
    	+ avi - new 
      + bali - old 
      + madi - now 
      + sunny - sun 

2. premisiones
  - grant the administration cluster abilities to user bali .
  - grant the role of project creating to madi 
  - remove the ability of project creating from sunny 
  - delete the kubeadmin user

3. manage users
  - create the following groups : 
    + gold , silver, bronze
  - add bali to gold 
  - add madi to silver 
  - add sunny to bronze




Manage Openshift container platform 
-----------------------------------

4. openshift project
  - meet the following requierments 
    + projects : 
       - food , cars , database
    +  grant the view role to bronze group in food 
    +  grant the edit role to sunny user in cars 






Control access to resources
---------------------------

5. create secret with Key:Value 
   - add the secret as env to deployment X 

10. create serviceaccount add scc set to deployment




Configure networking components
-------------------------------

11. create a secure route 


Configure pod scheduling
------------------------

6. go to namespace and manually add replicas to the deployment 


7. go to namespace and autoscale the deployment such and such 


8. create limitrange 
   - container :  cpu { max= 300m , min= 10m , deafult= 100m } , memory { max= 500Mi , min=5Mi , default= 100Mi}
   - pod : cpu { max= 300m , min= 10m } , memory { max= 500Mi , min=5Mi } 

9. create resourceQuota : 
   - pod 20
   - services 6  
   - replicascontroller 12
   - cpu 4
   - memory 1Gi

12. go to this and that namesapce and make the deployment work
  - reasons :
    +  node Selector
    +  resource requests 
