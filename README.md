# _FaultManagement
UserDemand for MW SDN based Fault Management

The current ComarchOSS based Fault Management is to be replaced by a set of microservices integrated into the application layer of the MW SDN domain.  

While IBM Netcool Operations Insight will be used as a user front end to perform management tasks, alarm notifications, lists and histories will also be made generally available to the entire application layer for automation purposes.  

The following tasks need to be performed in the background  
 - Consolidate alarm notifications from all devices into a single stream  
 - Recompute the references within the device notifications to be unique in the network context and to match the inventory content  
 - Update alarm lists and histories in the inventory based on device notifications  
 - Create alarm notifications based on changes within the inventory  
   - Reduce the number of notifications through aggregation and suppression (2)  
   - Offer subscriptions to all types of consumers  
 - Providing the alarm list of a specific device in the inventory (2)  
 - Updating the alarm list of a dedicated device in the inventory with current device content based on request (2)  
 - Automatically read device content when a gap is detected in the sequence of device notifications (3)  
 - Provide a domain interface for Netcool  
   - Managing the address of its subscription  
   - Reading the alarm list of a dedicated device from the inventory (2)  
  
The implementation of the tasks listed above follows an incremental approach.  
If not included in the initial setup, a number indicates the implementation phase.  
