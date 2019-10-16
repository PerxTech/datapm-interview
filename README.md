# datapm-interview

## A) Product Design

### Persona: 

Marketing Manager - Ulia

### Goal: 

To provide campaign insights and trends to our client who is a marketing manager at a telco company.

### How: 

Download the .csv and design dashboard cards using relevant data sets. 

### Intent: 

We would like to story-tell with the high volume of campaign related information received. Client should be able to understand the campaign performance based on the dashboard. These insights will then be used for retargeting in future campaigns.

### Assumptions:

- Campaign captures user demographic such as age, DoB, location, race, address, gender etc
- Third party data can be retrieved to support in-depth analysis (e.g. Facebook ads, Google Analytics etc)

### Inspirations:

- Google Analytics dashboard
- Business Intelligence dashboard

### Tasks:

Identify suitable data sets to define usable data charts/graphs

## B) SQL Test

### Prerequisite:

* BigQuery Account.
* Required CSV files are in folder `./data`, import into BigQuery in three diffrent tables as mentioned below. (BigQuery's free quota should be enough for this exercise)

* Table and Relation:
 1.  Campaign (id , name , updated_at)
 2.  Reward_camapigns( id , Reward_name , updated_at, campaign_id(FK(campaign.id)))
 3.  Reward_transactions(id, status, updated_at, Reward_camapigns_id(FK(Reward_camapigns.id)) )

### Use Case 1:

Client X would like to identify the most popular engagement day and time between a specific date range (Database stored data is in UTC format and input will be in SGT) for a Campaign.
 
   * Expected Output:
           No Of Transaction | Date | Time 

### Use Case 2:
         
Client X would like to see the weekly breakdown of reward performance along with comparison of previous week.

   * Expected Output:
          Reward name | Reward Redeemed count | Percentage difference as per previous week | Date/ Week 

### Deliverable

BigQuery SQLs with output.
