# jmeter-expandtesting_api

API testing in [expandtesting](https://practice.expandtesting.com/notes/api/api-docs/). This project contains basic examples on how to use JMeter to test performance API tests. 

# Pre-requirements:

| Requirement                     | Version        | Note                                                            |
| :------------------------------ |:---------------| :-------------------------------------------------------------- |
| Java                            | 8u202          | -                                                               |
| JMeter                          | 5.6.3          | -                                                               |  
| JMeter Plugins Manager          | 1.10           | -                                                               | 
| jpgc - Standard Set             | 2.0            | -                                                               | 

# Installation:

- See [Java SE 8 Archive Downloads](https://www.oracle.com/java/technologies/javase/javase8-archive-downloads.html), download the proper version for your OS and your JMeter and install it by keeping the preferenced options.
- Right click :point_right: **My Computer** and select :point_right: **Properties**. On the :point_right: **Advanced** tab, select :point_right: **Environment Variables**, :point_right: **New** in System Variables frame and create a variable called JAVA_HOME containing the path that leads to where the JDK software is located (e.g. C:\Program Files\Java\jdk1.8.0_202).
- Right click :point_right: **My Computer** and select :point_right: **Properties**. On the :point_right: **Advanced** tab, select :point_right: **Environment Variables**, and then edit Path system variable with the new %JAVA_HOME%\bin entry.
- See [JMeter download](https://jmeter.apache.org/download_jmeter.cgi) and download apache-jmeter-5.6.3.zip. Extract it in the prorject directory. Access bin folder and look for ApacheJMeter.jar file. Double click it to execute it.
- See [JMeter Plugins Manager](https://jmeter-plugins.org/wiki/PluginsManager/) and download jmeter-plugins-manager-1.10.jar. Paste it into JMeter's lib/ext directory. Restart JMeter to conclude the installation of JMeter Plugins Manager.
- Hit :point_right:**Options**, :point_right:**Plugins Manager**, :point_right:**Available Plugins**, check :white_check_mark:**jpgc - Standard Set** and :point_right:**Apply Changes and Restart JMeter** to install jpgc - Standard Set plugin. 

# Tests:

- On Windows Command Prompt, execute ```cd apache-jmeter-5.6.3/bin && jmeter -n -t expandtesting.jmx -l ../../csv_reports/report.csv -e -o ../../reports``` to run expandtesting collection, generate a .csv report in csv_reports folder and generate a .html report in reports folder.

# Support:

- [expandtesting API documentation page](https://practice.expandtesting.com/notes/api/api-docs/)
- [expandtesting API demonstration page](https://www.youtube.com/watch?v=bQYvS6EEBZc)
- [Stepping Thread Group](https://jmeter-plugins.org/wiki/SteppingThreadGroup/)
- [JMeter Beginner Tutorial 17 - How to setup realistic performance test-PACING](https://www.youtube.com/watch?v=cOPnXUDmTBY)
- [Jmeter 04 API Chaining](https://www.youtube.com/watch?v=BwZ2plCobSE)
- [issue using variable for Assertions in response in Jmeter](https://stackoverflow.com/a/66132429/10519428)
- [__javaScript](https://jmeter.apache.org/usermanual/functions.html#__javaScript)
- [Jmeter 5.5 error with assertion value type, string not equal to int](https://stackoverflow.com/a/74537909/10519428)
- [__RandomFromMultipleVars](https://jmeter.apache.org/usermanual/functions.html#__RandomFromMultipleVars)
- [Handle negative cases in JMETER, for example my expected output response is 400](https://stackoverflow.com/a/59533081/10519428)
- [13 | JMeter | HTML Reports from GUI & CMD |](https://www.youtube.com/watch?v=S8eO-jrQFpQ)
- [How do I run two commands in one line in Windows CMD?](https://stackoverflow.com/a/8055390/10519428)
- [Apache JMeter Github Action](https://github.com/marketplace/actions/apache-jmeter)

# Tips:

- UI and API tests to send password reset link to user's email and API tests to verify a password reset token and reset a user's password must be tested manually as they rely on e-mail verification. 
- JMeter, even with the jpgc - Standard Set plugin support, is not able to execute a ramp down procedure. Threads are abruptly removed according to the number of threads to be removed per second.
- Stteping thread groups can be configured for Load, Stress, Spike, Breakpoint and Soak tests. Configure the stepping thread group, following the instructions in the config pictures, according to the test type that must be tested.

