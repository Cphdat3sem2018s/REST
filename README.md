# REST (RESTful Webservices) with JAX-RS

## Learning Goals
After this week, you should:
  * Understand the principles of RESTful APIs.
  * Be able to implement a REST API using Java's JAX-RX API
  * Be able to implement a JSON API in java, using google's GSON library.
  * Be able to handle both success and error responses in a REST API

## Business competences
REST has become the current standard for designing web APIs, and is used for
virtually everything on the internet.

These lessons will provide the student with the necessary background to build
RESTful APIs in java.
## Plan

### Day1 - Rest principles and initial JAX setup and endpoints.

Remember to install [Postman](https://www.getpostman.com/)

### Day2 - Continuation from day 1, and data-transfer objects (DTOs)

### Day3 - Errorhandling with REST, and deployment to Digital Ocean

## Resources: 

### General

### Day1 Introduction to REST

Read:
  * [RESTfull Web Services](http://www.drdobbs.com/web-development/restful-web-services-a-tutorial/240169069?pgno=1) (There are 3 pages)

When you need it, you can see a quick summary of the most important annotations
used with JAX here:
  * [link](http://docs.oracle.com/javaee/6/tutorial/doc/gilik.html)

If you need more in-depth information (in later projects for example), jersey
(the JAX implementation we use) has a user guide:
  * [jersey user guide](https://jersey.github.io/documentation/latest/index.html)

After the dependency confusion in the ORM week, I'm just going to state it here:
we use two dependencies when creating RESTful webservices:
  * org.glassfish.jersey.bundles: jax-rs-ri  
    For the JAX-RS implementation we use (jersey)
  * com.google.code.gson: gson  
    For serializing and deserializing java objects to/from JSON.

Lecture materials:
  * [slides](Day1/slides.pdf)
  * [Demo](https://github.com/Cphdat3sem2018s/RestDemo18/)

For those who asked, Christian made [this video](https://www.twitch.tv/videos/172198991) going through the JAX setup and implementation of a small service.
The steps boil down to:
  1. Create a new Maven web application
  2. Add the jax-rs-ri dependency (and the gson dependency if you need it)
  3. Create a new "restful web service from pattern"

<!--
- [JAX-RS Intro](https://efif.sharepoint.com/sites/cph/Lyngby/_layouts/15/guestaccess.aspx?docid=096689c5617a1453786e2401a34858af8&authkey=AUj8EbepY-ohhgVLk3Z2klU) 

**Clone this [repo](https://github.com/Lars-m/restClassDemoDay1.git)** to get what we did in the class
-->

### Day2 - Continuation from day 1, and data-transfer objects (DTOs)

Read:
  * [Wikipedia article about DTOs](https://en.wikipedia.org/wiki/Data_transfer_object)

<!--
The fetch api is documented
[here](https://developer.mozilla.org/en/docs/Web/API/Fetch_API).
A pretty indept tutorial can be [found
here](https://developers.google.com/web/updates/2015/03/introduction-to-fetch)
-->

### Day3 - Errorhandling with REST, and deployment to Digital Ocean

We map java exceptions to http error responses, as well as create responses
(errors included) from scratch.

Read:
  * [JERSEY documentation](https://jersey.github.io/documentation/latest/representations.html#d0e6352). section 7.3
    on creating error responses via exceptions and mapping existing exceptions to
    error responses.

  * The JAX class for representing responses (aptly named `Response`) is
    documented
    [here](http://docs.oracle.com/javaee/7/api/javax/ws/rs/core/Response.html).  
    Do not read through this, but use it as needed. It may be helpful to have
    Looked the method summary over briefly.

## Exercises 

### A word on difficulty levels:
As you have seen on previous semesters, we use color the colors GREEN, YELLOW
and RED to indicate the level of difficulty/work intensity in the exercises for
the concurrency exercises. The colors can’t be directly translated to exam
grades, but can help you in two ways:
  1. If you feel that the green exercises are a challenge, the red ones may not
     be a good use of your time for now.
  2. If you are pressed for time, the most efficient use of it is probably to
     focus on the green and yellow exercises, and come back to the red ones
     later if possible.

| Level | Expectation |
| ------ | ----------- |
| Green | |
| Yellow ||
| Red | |

  * [Exercise Day1](https://docs.google.com/document/d/1jN5Kfo8jdYgcBxYML6WBY_BPpdBQJbVibhU0FcnpI2k/edit?usp=sharing) Rest principles.

<!--
 
  * [Exercises Day-1](https://docs.google.com/document/d/1zezTIruAiSkhhNCRHJh4EYOcf_mgMblGs6U_XmQ3vp4/edit?usp=sharing) (Basic thread creation and raceconditions)
  * [Exercises Day-2](https://docs.google.com/document/d/1A3rBzbbppVZKx-YrGJKWdgsWKs8xNrTR2BeG7zVu6hg/edit?usp=sharing) (Producer/Consumer and Deadlocks)
  * [Exercises Day-3](https://docs.google.com/document/d/1AkC59GQm5sbwWpKkideE9kI9KmbscIwKOygn9b_FJMU/edit?usp=sharing) (Using an executor service)
  * [StudyPoint Exercise](https://docs.google.com/document/d/1_joY_2_fkswWzPwWUmfYYL2GXpWs23vfiOqXwMqiqmI/edit?usp=sharing)
  -->
<!--

[this guide](https://docs.google.com/document/d/1TnPFlZjl8phGqROQB0syUnSJQiaDASZya3gv8qK2qcI/edit?usp=sharing) contains info on how to access logs on deployed webservices
## Exercises 
[Exercise - REST Quotes](https://drive.google.com/open?id=13iWLS-XQZLtalNf-6ER3uJwyaPy0rw-OACC7Z6Tv7N8)<br>
[Exercise - REST Quotes ErrorHandling](https://drive.google.com/open?id=1R8w8CfN12ZHJAqb7nK9ZApsqDTMZsIRBvHJSc1m9cPY)<br>
[Exercise - REST Persons](https://drive.google.com/open?id=10UpxEHPBtdMpnlwVjVI-wNkoEAuoglD2HY_ofKo5yxI)<br>
[Exercise - REST Persons ErrorHandling](https://drive.google.com/open?id=1VD-_3QHWrP-asOArc786JGAtlVkjhu6Iaj8UHfWByyg)<br>
[Exercise - REST Digital Ocean](https://drive.google.com/open?id=1D92Eynuh4YmIttOUWJtgmcWiTl9t1hWFdsJaYQgKI_E)<br>
[Exercise - REST RestAssured GettingStarted](https://drive.google.com/open?id=13JAp6RUOozBKfK5-Cxr8L2z49wypqb2_N38XcmtFRtM)<br>
[Exercise - REST RestAssured Continued](https://drive.google.com/open?id=1mMnFJgoCo2_Lgomwckz8RDttu9VV4a-_SE2xoGQOk5Y)

## Study point exercises
[Study point exercises](https://drive.google.com/open?id=1aqJx93Y9fROeYq6xbneWoBstVeDXIn00vimT0AWqaPk)

-->
<!--
-->
