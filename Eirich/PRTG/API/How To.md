PRTG includes a web-based REST API (Application Programming Interface) that enables external programs to access information from the monitoring database and to manipulate objects inside the database of PRTG.

In the context of the PRTG HTTP API the attribute "REST" essentially means:

- It is HTTP/HTTPS based.
- It uses a set of "HTTP GET" URLs to access and manipulate the data.
- ==**You get back an XML document in return for most calls.**==

The PRTG HTTP API offers the following features:

- Authentication, error handling, and optional encryption
- Functions to get live object and status data as well as live graphs
- Functions to get historic sensor data and graphs
- Functions to manipulate objects (for example, edit, add, or delete)


All calls to the PRTG HTTP API are performed by HTTP GET requests. The URLs consist of a path to the API function and some parameters. Here are two example calls:

- Sample Call 1:
    
    https://yourserver**/api/table.xml**?content=sensortree
    
- Sample Call 2:
    
    https://yourserver**/api/rename.htm**?id=objectid&value=newname
    

The first part of the URL ( **/api/table.xml** or **/api/rename.htm**) addresses an API function. In these examples, the functions either render a table in XML format or rename an object. The second part after the question mark contains a number of parameters for additional control.

==**Important:** PRTG expects all data in the GET parameters to be UTF-8 encoded and URL-encoded.==


https://ehprtg01/api/historicdata.xml&avg=0&sdate=2025-10-01-00-00-00&edate=2025-10-20-00-00-00?content=topdata&columns=position%2Cvalue_%2Cobjid%2Cbaselink&sortby=-value_2V&topnumber=-1&id=17846&subid=2&username=prtgadmin&password=!Z7I95S!

https://ehprtg01/api/table.xml?content=topdata&columns=position%2Cvalue_%2Cobjid%2Cbaselink&sortby=-value_2V&topnumber=-1&id=17846&subid=2&username=prtgadmin&password=!Z7I95S!