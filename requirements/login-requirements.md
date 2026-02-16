# Trendyol Login Feature - Requirements

Application: Trendyol Web  
Feature: Login  
Test Type: Manual Testing
---

#### Note
The requirements document was created after writing the login test cases and login bug reports, in order to demonstrate reverse-engineering skills and understanding of system behavior. User stories are related to the corresponding login test case number.



### User Story-01: Login with valid credentials

As a registered user  
I want to log in using a valid email address and password  
So that I can access my account

#### Acceptance Criteria (BDD)

Scenario: Successful login with valid credentials  
Given the user has an existing account  
And the user is on the login page  
When the user enters a registered email address and correct password  
And clicks the "Giriş Yap" button   
Then the user should be logged in successfully  
And redirected to the home page



### User Story-02: Login attempt with invalid password

As a registered user  
I want to get an error message indicating that my email or password is not correct when I log in using a valid email address and an invalid password  
So that I can correct my password and successfully log in

#### Acceptance Criteria (BDD)

Scenario: Login attempt with invalid password
Given the user has an existing account  
And the user is on the login page  
When the user enters a registered email address and an invalid password  
And clicks the "Giriş Yap" button   
Then the user should see an error message indicating that the email or password is incorrect

**Note:** Acceptance Criteria are derived from observing the actual behavior of the Trendyol login page.



### User Story-03: Login attempt with empty email field

As a user  
I want to get a validation message indicating that I should enter an email address when I try to log in without entering an email address  
So that I can enter my email address and continue the login flow

#### Acceptance Criteria (BDD)

Scenario: Login attempt with empty email field
Given the user is on the login page
When the user leaves the email input field empty  
And clicks the "Devam et" button   
Then the user should see an validation message indicating that an email address must be entered



### User Story-04: Login attempt with invalid email

As a user  
I want to see a validation message when I try to log in with an invalid email address  
So that I can correct my email address and continue the login process

#### Acceptance Criteria (BDD)

Scenario: Login attempt with invalid email format  
Given the user is on the login page  
When the user enters an invalid email address  
And clicks the "Devam Et" button  
Then the user should see a validation message indicating that the email address format is invalid

