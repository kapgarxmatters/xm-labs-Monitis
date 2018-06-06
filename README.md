
# Monitis
Monitor your web performance and reliability for websites, servers, networks & applications.  This version of the integration is one way and is used when an alert is created in Monitis.  

<kbd>
  <img src="https://github.com/xmatters/xMatters-Labs/raw/master/media/disclaimer.png">
</kbd>

# Pre-Requisites
* Monitis SaaS - If you don't have one, [get one](http://www.monitis.com)!
* xMatters account - If you don't have one, [get one](https://www.xmatters.com)!

# Files
* [ExampleCommPlan.zip](ExampleCommPlan.zip) - This is an example comm plan to help get started. (If it doesn't make sense to have a full communication plan, then you can just use a couple javascript files like the one below.)
* [EmailMessageTemplate.html](EmailMessageTemplate.html) - This is an example HTML template for emails and push messages. 
* [FileA.js](FileA.js) - An example javascript file to be pasted into a Shared Library in the Integration builder. Note the comments

# How it works
Add a Contact in Monitis using the webhook type.  Use the contact for any alert rules.  When an alert is created, Monitis will send the information to xMatters to notify the on-call resource.

# Installation
Details of the installation go here. 

## xMatters set up
1. Steps to create a new Shared Library or (in|out)bound integration or point them to the xMatters online help to cover specific steps; i.e., import a communication plan (link: http://help.xmatters.com/OnDemand/xmodwelcome/communicationplanbuilder/exportcommplan.htm)
2. Add this code to some place on what page:
   ```
   var items = [];
   items.push( { "stuff": "value"} );
   console.log( 'Do stuff' );
   ```


## Application ABC set up
1. In your Monitis account, create a Contact.  http://www.monitis.com/support/alerts/alerting-via-webhook-contact
2. When you add your contact to a rule, you will have to verify the contact.  xMatters won't do that, so you will need to copy and paste the following url into a browser.
http://monitis.com/confirmation/userkey/confirmContact/contactId/code”
http://monitis.com/confirmation/1MKCDQ2J2DD2JGQ1O3F6M8R030/confirmContact/https://advisors.na5.xmatters.com/api/integration/1/functions/cf91c7d3-d8f1-4f53-8d2d-bb387b5db58c/triggers?apiKey=50b04be6-f7c0-4c11-90fe-8daf900c4f0c/code


# Testing
Be specific. What should happen to make sure this code works? What would a user expect to see? 

# Troubleshooting
Optional section for how to troubleshoot. Especially anything in the source application that an xMatters developer might not know about, or specific areas in xMatters to look for details - like the Activity Stream? 
