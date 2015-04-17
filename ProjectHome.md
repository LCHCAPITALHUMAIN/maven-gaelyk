# About #
Use the maven-gaelyk archetype to create a best practices Maven Gaelyk project.  This provides the quickest and least painful way to be up and running on the app engine in a matter of seconds.  The only prerequisite is that you have Maven installed.

## Releases ##
05/17/11 - 0.7.0 - gaelyk-archetype - Support for Gaelyk 0.7.0 + App Engine 1.5.0 <br />
01/12/11 - 0.6.1 - gaelyk-archetype - Support for Gaelyk 0.6.1 + App Engine 1.4.0 <br />
10/15/10 - 0.5.6 - gaelyk-archetype - Simplified POM! Support for Gaelyk 0.5.6 + App Engine 1.3.8 <br />
10/07/10 - 0.5.5 - gaelyk-archetype - Support for Gaelyk 0.5.5 + Groovy 1.7.5 + App Engine 1.3.7 <br />
10/04/10 - 0.5.0 - gaelyk-archetype - Support for Gaelyk 0.5.0 + Groovy 1.7.5 + App Engine 1.3.7 <br />
08/11/10 - 0.4.3 - gaelyk-archetype - Support for Gaelyk 0.4.3 + Groovy 1.7.4 + App Engine 1.3.5 <br />
05/10/10 - 0.4.1 - gaelyk-archetype - Minor bug fix.  Includes missing dependency. <br />
05/08/10 - 0.4.0 - gaelyk-archetype - Creates a Gaely v0.4 Template Project that can be immediately deployed to the app engine.

10/07/10 - 0.5.5 - Spring Security 3.0.3 RELEASE with Gaelyk 0.5.5 + Groovy 1.7.5+ App Engine 1.3.7 <br />
10/04/10 - 0.5.0 - Spring Security 3.0.3 RELEASE with Gaelyk 0.5.0 + Groovy 1.7.5+ App Engine 1.3.7 <br />
05/17/10 - 0.4.0 - gaelyk-security-archetype - Initial release of the Gaelyk v0.4 Template project w/ Spring Security

## Groovy to the App Engine in 3 simple steps w/ Maven & Gaelyk ##
(<strong>No</strong> <a href='http://code.google.com/appengine/'>App Engine SDK</a> / <a href='http://groovy.codehaus.org/'>Groovy</a> / <a href='http://gaelyk.appspot.com/'>Gaelyk</a> Download Required)

- This following assumes you have Apache <a href='http://maven.apache.org/download.html'>Maven</a> installed.

1. Create the Gaelyk Template Project (Assuming you want to deploy to an App Engine id of myapp)

```
mvn archetype:generate -DarchetypeGroupId=org.codeconsole \
-DarchetypeArtifactId=gaelyk-archetype -DarchetypeVersion=0.7.0 \
-DartifactId=gaelykapp -DgroupId=com.appspot.gaelyk \
-DgaeApplicationName=gaelykapp \
-DarchetypeRepository=http://maven-gaelyk.googlecode.com/svn/repository/
```
(If you are on Windows, you will need to remove the \'s or copy from the Windows section at the bottom of the page)
Note: Substitute the values for artifactId, groupId, and gaeApplicationName with your own.

2. Change directory to your newly created app.
```
cd gaelykapp
```
3. Deploy it!  (http://gaelykapp.appspot.com/)
```
mvn package gae:deploy
```
or Run it (http://localhost:8080/)
```
mvn package gae:run
```

<a href='http://www.twitter.com/codeconsole'><img src='http://twitter-badges.s3.amazonaws.com/follow_me-a.png' alt='Follow codeconsole on Twitter' /></a>

Note: Alternatively you can run:
```
mvn archetype:generate -DarchetypeGroupId=org.codeconsole -DarchetypeArtifactId=gaelyk-archetype \
-DarchetypeVersion=0.7.0 -DarchetypeRepository=http://maven-gaelyk.googlecode.com/svn/repository/
```
and Maven will prompt for the Artifact Id, Group Id, Google App Id




Windows Maven Command:
```
mvn archetype:generate -DarchetypeGroupId=org.codeconsole -DarchetypeArtifactId=gaelyk-archetype -DarchetypeVersion=0.7.0 -DarchetypeRepository=http://maven-gaelyk.googlecode.com/svn/repository/ -DartifactId=gaelykapp -DgroupId=com.appspot.gaelyk -DgaeApplicationName=gaelykapp
```


# Gaelyk With Spring Security #

#summary Gaelyk with Spring Security

# Introduction #

This first version of the gaelyk-security-archetype sets up a template project with basic Spring Security configured.  This archetype does not include the upcoming Gaelyk Security plugin that provides Datastore backing (currently xml backing) and registration.  It is just something to point you in the right direction up until the official release which should be early next week 10/11/10.

# Details #

Run the following maven command to create a new Gaelyk Template project with Spring Security:
```
mvn archetype:generate -DarchetypeGroupId=org.codeconsole \
-DarchetypeArtifactId=gaelyk-security-archetype -DarchetypeVersion=0.5.5 \
-DarchetypeRepository=http://maven-gaelyk.googlecode.com/svn/repository/
```

Enter a artifact id (name of your application)
Enter a group id (how you want to package it, usually your domain name backwards)
Enter your Google App Engine app id

Alternatively, you can skip the prompts and pass the above parameters in one command:

Run the following maven command to create a new Gaelyk Template project with Spring Security:
```
mvn archetype:generate -DarchetypeGroupId=org.codeconsole \
-DarchetypeArtifactId=gaelyk-security-archetype -DarchetypeVersion=0.5.5 \
-DarchetypeRepository=http://maven-gaelyk.googlecode.com/svn/repository/ \
-DartifactId=gaelykapp-security -DgroupId=com.appspot.gaelyk \
-DgaeApplicationName=gaelykapp-security
```

To run your app locally, type
mvn gae:run

Try to view a private page (default admin username/password is: admin@gaelykapp.com/admin:
http://localhost:8080/admin

to deploy to the App Engine, type:
mvn gae:deploy
then enter your email/password

Try to view a private page:
http://gaelykapp-security.appspot.com/admin



Windows Maven Command:
```
mvn archetype:generate -DarchetypeGroupId=org.codeconsole -DarchetypeArtifactId=gaelyk-security-archetype -DarchetypeVersion=0.5.5 -DarchetypeRepository=http://maven-gaelyk.googlecode.com/svn/repository/ -DartifactId=gaelykapp-security -DgroupId=com.appspot.gaelyk -DgaeApplicationName=gaelykapp-security
```