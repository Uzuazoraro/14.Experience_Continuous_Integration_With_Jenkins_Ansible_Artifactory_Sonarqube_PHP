# 14.Experience_Continuous_Integration_With_Jenkins_Ansible_Artifactory_Sonarqube_PHP

I will be setting up a CI/CD Pipeline for a PHP based application.

This project has two repositories .Each contains its own CI/CD pipeline written in a Jenkinsfile. The directories are:

1. ansible-config-mgt REPO: this repository contains JenkinsFile which is responsible for setting up and configuring infrastructure required to carry out processes required for our application to run. It does this through the use of ansible roles. This repo is infrastructure specific

2. PHP-todo REPO : this repository contains jenkinsfile which is focused on processes which are application build specific such as building, linting, static code analysis, push to artifact repository etc
Prerequisites
Will be making use of AWS virtual machines for this and will require 6 servers for the project which includes: Nginx Server: This would act as the reverse proxy server to our site and tool.

Jenkins server: To be used to implement your CI/CD workflows or pipelines. Select a t2.medium at least, Ubuntu 20.04 and Security group should be open to port 8080

SonarQube server: To be used for Code quality analysis. Select a t2.medium at least, Ubuntu 20.04 and Security group should be open to port 9000

Artifactory server: To be used as the binary repository where the outcome of your build process is stored. Select a t2.medium at least and Security group should be open to port 8081

Database server: To server as the databse server for the Todo application

Todo webserver: To host the Todo web application.

