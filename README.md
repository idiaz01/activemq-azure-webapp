# Apache ActiveMQ on Azure WebApps

### ActiveMQ configuration
In order to set up the message exchange through http the following connector should be declared in apache-activemq-5.15.2\confactivemq.xml
<transportConnector name="http" uri="http://0.0.0.0:${HTTP_PLATFORM_PORT}?maximumConnections=1000&amp;wireFormat.maxFrameSize=104857600"/>

### WebApp configuration file (web.config)
The main line in this file is:
<httpPlatform processPath="D:\home\site\wwwroot\run_activemq.bat" arguments="" stdoutLogEnabled="true" startupRetryCount='10'></httpPlatform>
This line calls run_activemq.bat to run Apache ActiveMQ when the WebApp starts.

### run_activemq.bat
Runs the activemq.jar file with the required parameters.
Note that this version uses the JDK version 1.8.0_11.

## WebApp configuration
- Java Version: 8
- Java Minor Version: Newest
- Platform: 32-bit

### This repo has been done in collaboration with Iván Diaz (https://github.com/idiaz01)


License
----

MIT