# logicaldoc-ce-hsqldb
Docker project for LogicalDOC Community (ready to use with HSQLDB embedded database)

LogicalDOC is a Web-based open source document management system. By leveraging on the best-of-breed Java frameworks, it creates a flexible and powerful document management platform, which thanks to the most advanced presentation technology, is able to meet the needs of usability and more demanding management. For further reading https://www.logicaldoc.com


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

After the image is started for the first time, you will be able to connect with a browser at http://localhost:8080

To access the system at login use admin/admin as credentials.
