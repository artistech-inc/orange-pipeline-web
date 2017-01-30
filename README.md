# Git Repo for orange Pipeline Web-App

This is a web-app which will utilize various 3rd party apps/scripts for extracting entity information from documents.

## Version 1.2

- Initial version of JIE Multimedia

## Downloading

```sh
git clone https://github.com/artistech-inc/pipeline-base.git
cd pipeline-base
mvn clean install
cd ..
git clone https://github.com/artistech-inc/orange-pipeline-web.git
cd orange-pipeline-web
mvn clean package
```

## Configuration

Update the [WEB-INF/web.xml](https://github.com/artistech-inc/orange-pipeline-web/blob/master/src/main/webapp/WEB-INF/web.xml) file. Each Servlet that utilizes an external application/script/process must have the path to the application set. For now, this includes:

- joint_ere
- ENIE
- Merge Tool
- Visualization Generation

Along with the web.xml file, the [META-INF/context.xml](https://github.com/artistech-inc/orange-pipeline-web/blob/master/src/main/webapp/META-INF/context.xml) must be configured. The `data_path` value must be somewhere that Tomcat can write to.

## Compilation

This project should be able opened using Netbeans as a Maven Web-App. It will automatically detect the type of project.  
The project can also be compiled on the command line directly using maven.  
Depends on pipline-base project.  See above.

## Deployment

The output from compilation is in the `target/` directory as `orange-pipeline-web-1.2.war`. This war can be deployed to Tomcat's `webapps` directory. Once deployed, it can be accessed via `http://<ip_address:port>/orange-pipeline-web-1.2/`.

## Bugs

- Issues and bugs can be e-mailed or registered.

## TODO

- Output console
- Delete data with session timeout

## Future (possibly not in scope)

- Database
- Users
