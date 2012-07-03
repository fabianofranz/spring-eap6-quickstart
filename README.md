Spring Framework on OpenShift with JBoss EAP 6
==============================================

What is it?
-----------

This is a sample Maven 3 project to help you get your foot in the door developing with Spring on JBoss Enterprise Application Platform 6 or JBoss AS 7.1, deployable on OpenShift (PaaS by Red Hat).

This project is setup to allow you to create a compliant Spring 3.1 application using Spring MVC, JPA 2.0 and Bean Validation 1.0. It includes a persistence unit and some sample persistence and transaction code to introduce you to database access in enterprise Java. 

Quickstart
----------

1) Create an account at http://openshift.redhat.com/ and follow the Getting Started guide to install the OpenShift command line tools.

2) Create a JBoss Enterprise Application Platform 6 app:

    rhc app create -a spring -t jbosseap-6.0

3) Add this upstream repo:

    cd spring
    git remote add upstream -m master git://github.com/fabianofranz/spring-eap6-quickstart.git
    git pull -s recursive -X theirs upstream master

4) Then push the repo upstream

    git push

5) That's it, you can now browse to your application at:

    http://spring-$yournamespace.rhcloud.com


The example uses the `java:jboss/datasources/SpringQuickstartDS` in-memory database, configured and deployed by the application.

