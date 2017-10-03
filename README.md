The purpose of this github project is to allow a candidate to demonstrate the
to communicate software development concepts while writing python-django code.


Introduction
============

This is a project that is meant to display how you think about 
your craft. You will _NOT_ be evaluated on polish and perfection.  Choose your 
efforts carefully and simply be ready to defend the priority choices you 
make. (Just like any other job.)

The expectation is 3 to 5 hours of time. You are welcome to take more if you 
like. There is no restriction. You may google all you like.

Setup Instructions
------------------

* Fork and clone this repo
* Issue the `vagrant up` command

At this point you have a working run time that has nginx, uwsgi installed.

You application should go in `/opt/harper` on the guest, however you can 
develop in the `./harper` directory on your workstation.

The configuration of the guest was done with Ansible.

**IMPORTANT**: 

You may continue to use Ansible to configure the guest or you can simply 
directly install what you need. How you choose to do this will be a topic
of discussion. (e.g. why did you made the choice)

**IMPORTANT**: 

No database has been installed. Use what you like, be ready to discuss the 
choice and its relative merits.

**IMPORTANT**: 

There are bugs in the configuration of `nginx` and `uwsgi`.  Document the
issues in the Github issue tracker of your forked project and fix them. Be
ready to discuss the makings of a good bug report and your workflow.

Task
----

Create a simple application to manage hotels, their location and their contacts.

Requirements
++++++++++++

_Data_:

* A hotel can have many contacts.
* Countries have many regions 
* Regions have many states
* Hotels can have locations in one or more states

Use Django migrations to create models and tables.  Remember you will need to
install a database.

Be ready to discussion the relative merits of your data model. 

_Application Bootstrap_:

* Use fixtures to populate a minimum of 10 hotels in 2 countries.  

_Application Requirements_:


Back end:

* Use something simple/elegant to write a back end maintenance system for 
  applicaiton data.  
* A business owner should be able to maintain the data in each table you create.
* Using the Django Admin is fine.
 
API:

Required:

* Create an endpoint that allows a request to pull a list of individual hotels.
* Create an endpoint that allows a request to pull the contacts for a give hotel.

These endpoints must be part of the submission.

User Interface:

* The user navigates to a hotel page and is presented with a truncated list of 
  all hotels. They should be able to sort and filter the presented list.
* The user navigates to a contact page and selects a hotel. They are 
  presented with contact information for the property. 

Criteria
========

The evaluator should be able to clone your enviroment, issue a vagrant up and
operate the system you've creatd. 

The role of a developer in an organization is about communication. Your 
submission will be evalutated based on the following:

* Does it work. (Hotels, countries, regions, etc will be added and pages will
  be checked.)
* Code readability, commenting and maintainability.
* Your ability to make the run time enviroment work (installing a database, 
  configuring uwsgi and nginx)
* How did you organize work you uncovered but chose not to do during the 
  project. 
* How did you build the run time environment and how would you do it in 
  a professional situation. 

Extra Credit:
* Keep a wiki in your project of improvements you'd make to this project.
* Keep you deferred work in the Github issue tracker and lay out a simple 
  workflow.
* Add a feature not listed in the requirements and be ready to discuss why.







