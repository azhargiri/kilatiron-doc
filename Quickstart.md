# CloudKilat Quickstart

It's easy to start with CloudKilat. Follow this 5 minute quickstart to get your first app running on CloudKilat PaaS.

**Note:** All examples starting with $ are supposed to be run in a terminal. For Windows we recommend using Git bash, which comes bundled with the Windows Git installer. Throughout this quickstart and the rest of the documentation placeholders are marked by being written all uppercase.

## Install the Required Software

### Requirements

* git version control system
* ironuser/ironapp command line client

### Install git

Install Git from the [official site](http://git-scm.com/) or your package repository of choice. For Windows it's recommended to use the official installer and Git bash. Come back when you are done.

### Install ironcli

**Linux/Mac OS X:** We recommend installing ironcli via pip.

~~~bash
# if you don't have pip yet
$ sudo easy_install pip
$ sudo pip install ironcli
~~~

**Windows:** Please download the provided [installer](https://download.kilatiron.net/windows).

## Create a User Account (if you haven't already)

You can register on [our website](www.cloudkilat.com).

## Add a Public Key

~~~bash
$ ironuser key.add
Email   : EMAIL
Password: PASSWORD
~~~

The command line client will determine if you already have a public key and upload that or offer to create one.

## Create the First Application on CloudKilat

Create a new application on the CloudKilat platform by giving it an unique `APP_NAME` (the name is used as the `.kilatiron.net` subdomain) and choosing the `TYPE`.

~~~bash
$ ironapp APP_NAME create [java, php, python, ruby, nodejs]
~~~

If the `APP_NAME` is already taken, please pick another one.

Change to the working directory where you want to store your source code.

~~~bash
$ cd PATH_TO/YOUR_WORKDIR
~~~

Clone one of the example apps in your preferred programming language and push it to the CloudKilat platform.

~~~bash
# for Java
$ git clone https://github.com/cloudControl/java-jetty-example-app.git
$ cd java-jetty-example-app

# for PHP
$ git clone https://github.com/cloudControl/php-silex-example-app.git
$ cd php-silex-example-app

# for Python
$ git clone https://github.com/cloudControl/python-flask-example-app.git
$ cd python-flask-example-app

# for Ruby
$ git clone https://github.com/cloudControl/ruby-sinatra-example-app.git
$ cd ruby-sinatra-example-app

# for Node.js
$ git clone https://github.com/cloudControl/nodejs-express-example-app.git
$ cd nodejs-express-example-app

# now push
$ ironapp APP_NAME push
~~~

The push fires a hook that prepares your application for deployment like pulling in requirements and more. You can see the output of the build process in your terminal.

## Deploy Your Application on CloudKilat

Deploy your app with

~~~bash
$ ironapp APP_NAME deploy
~~~

**Congratulations, your app is now up and running.**

~~~bash
http[s]://APP_NAME.kilatiron.net
~~~

## Cheatsheet

Grab [our cheatsheet (PDF)](https://github.com/cloudControl/kilatiron-doc/blob/master/Cheat%20Sheet%20Kilat%20Iron.pdf) to have the most important command line client commands handy at all times.

## Documentation

To learn more about all the platform features and how to integrate it seamlessly into the development life cycle please refer to the extensive [platform documentation](https://github.com/cloudControl/kilatiron-doc/blob/master/Platform%20Documentation.md).
