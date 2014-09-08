jobs
====

## current status
#### in development


## overview
```jobs``` manages services and the jobs submitted to those services.


## resources

* ```/services/<service-id>/queue```
* ```/services/<service-id>/jobs```
* ```/jobs/<job-id>```
* ```/services/<service-id>/info```


## API overview  
  * ```GET /services```  
    * returns list of available services
      * ```id``` : the UUID assigned to the service
      * ```short_name``` : a short code name, e.g., jhove, vxcode, axcode, bag_validation
      * ```summary``` : a brief summary of service's description
      * ```status``` : a status code e.g, ```up```, ```down```, ```paused```  

  * ```POST /services```
    * create new service

  * ```GET /services/<id>```
    * provides a detailed service description  

  * ```GET /services/<id>/status```
    * returns a detailed summary of the service
      * status
      * number of jobs per state
      * queue wait time

  * ```GET /services/<id>/template```
    * returns a sample job template


  * ```POST /services/<id>/queue```
    * creates a new task and returns the job id / and job URL for monitoring/control
	
  * ```GET /jobs```
    * returns list of all jobs

  * ```GET /jobs/<id>```
    * returns status and additional URLs, (e.g., details), for job <id> 
	
  * ```GET /jobs/<id>?q=details```
    * returns detailed job information including output


add stuff about querying by object id.
e.g., all jobs by object id.
