
# The Alpha

The Aplha is a most important and component of our ecosystem. It has the power to add or delete or modify the tenant actions. This is the where we handle out tenants, register our new services
developed by SCLabs, payment information of tenants, attach and detach services to the tenants, SF idp detials and all the collection detials and schema that are being used in all of the
products [Services].


# Database Desing

Before explaning the functionality, I'll start with database schema.

#### master

Master collection stores all the data which is necessary for native integration with SF as well the tenant_id with their associated database names, port and master credentials.

#### services

This collection maintains the list of products which are developed by SCLab, and a reverse mapping with the tenant_ids for analytics purpose.

#### serviceGods

This is where god of services store there access credentials. Each tenant(company) will have one or more than one attached services. We store the username and credentials which have the power to
access the database with all privileges

#### roles

This is where we are applying rbac[Role based access control], we have diferent types of roles which will be attached while creating any user for the tenant. There are universaly 4 types user
explained below.

* Gods [Super Super Admin]

The gods live and exists on the top layer of our ecosystem. They do not interfere in the human reaml as it's not wise to be known in lower realm that create a posibility of ecosystem our failure.
Due to this reason they have created multipule proxies of their own but with different abilities. They have the power to create, destroy, allow, deny, attach, detach, halt any service or process
in tenant realm. Gods have a collection named as serviceGods in Alpha database maintained by the SCLabs of Steppingcloud. Their credentials are encrypted and can only be seen bt those who have the
key for decryption. God of one tenant dosen't have the power to see on the world of other Gods, the are restriced by the tenant seperation.

Only SClabs have that key, and they are the creator of this real.

* Demi-Gods [Super Admin]

Demi-gods are one level down from the gods they have the same power as the Gods but confined by the services seperation. The services are the products developed by SClabs and demi-gods have the
accees to one serice only, one demi-god can't access other demi-god's possession.

* Kings [Admin]

Kings alse have the access to the service saperation but dosen't have the same level of authority as Demi-gods, demi-gods can create new Kings if he wants. King is responsible for managing and 
configuting and addeding humans the service realm.

* Humans [Users]

Humans in this ecosystem are the enduser's which will interact with the service.


# Functionality

Let's deep dive inot the functionality Âof the ALPHA.

#### Tenant Registration

Alpha is reponsible for adding new tenant into the ecosystem. It generate the tennant_id, username and password for accessing the tenant database and also manage the services attached to a tenant.

#### SFTP Refistration 



