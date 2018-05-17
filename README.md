# logicaldoc-ce-hsqldb
Docker project for LogicalDOC Community https://www.logicaldoc.com/download-logicaldoc-community

LogicalDOC is a multi-platform Web-based open source document management system. 
By leveraging on the best-of-breed Java frameworks, it creates a flexible and powerful document management platform, which thanks to the most advanced presentation technology, is able to meet the needs of usability and more demanding management. 

This distribution of LogicalDOC DMS uses with pre-installed HSQLDB database, the distribution itself is light and ready for use, however it is not recommended for production because it uses an embedded Java database 
(HSQLDB database engine http://hsqldb.org/).

LogicalDOC is a web-based document management system designed to handle large amounts of electronic documents.
It allows to organize and classify documents on multiple levels: in folders, using tags and classifying documents by type.
You can define new types of documents by specifying the various fields and their properties.

The software is localized in many languages: Russian, English, Chinese, Korean, Japanese, Italian and many others and one of its most interesting features is its ability to index the content of documents using different algorithms depending on the language of the document.
This allows later to perform "smart" full-text searches.

LogicalDOC Community provides a set of SOAP and REST API interfaces that allow the system to be integrated with other applications
The web-service API documentation is available in the LogicalDOC Documentation website https://docs.logicaldoc.com/en/web-services-api

In addition, a WebDAV and a CMIS interface are available.
Native apps for Android and iOS are published and available for free download on Google Play and iTunes.
   
For a complete list of features, take a look at https://www.logicaldoc.com/features


How to run:
open a console and execute (depending on your settings)

```Shell
docker run -p 8080:8080 logicaldoc/logicaldoc-ce-hsqldb
```

or

```Shell
sudo docker run -p 8080:8080 logicaldoc/logicaldoc-ce-hsqldb
```

another good way to start the application would be docker-compose, here is a sample file:

```
version: '2'
services:
 logicaldoc: 
  container_name: logicaldoc-ce
  image: logicaldoc/logicaldoc-ce-hsqldb
  ports:
   - 8080:8080
```

After the image is started for the first time, you will be able to connect with a browser at http://localhost:8080/logicaldoc

To access the system at login use admin/admin as credentials.
