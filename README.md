# MAGAZINE-MANAGEMENT-SYSTEM
This is an OOP project to create a Magazine Management System

ONLINE MAGAZINE MANAGEMENT SYSTEM

By: Khadijat Oparemi 

# Project Description

The aim of the project to is to build an online magazine management system where users can create account, log in, and personalize their reading preferences.Also Authors can submit artcle, and editors can review and publish them.

# Classes

  # Subscriber
-Properties: subscriberName, email, birth_year, password, subscriptionName, preferences

-Methods: authenticate, upgradeSubscriptionName, personalizePreferences

  # Subscription:
-Properties: subscription_id, subscriptionName, num_subscribers
-Methods: Signup

  # Article:
-Properties: title, content, author, publication_date

-Methods: Submit, review, publish


# CODE
1- SUBSCRIBER

#Define Subscriber class which represents the User's unique identifiers

class Subscriber:
     def __init__(self, name, email, birth_year, password, subscription_type, category):
        self.name = name
        self.email = email
        self._birth_year = birth_year
        self.__password = password
        self.subscription_type = subscription_type
        self.category = category
        

 #Authenticate user befor they can sign-in
 
    def authenticate(self, entered_password):
        Subscriber= input('Enter your username')
        password = input('Enter your password')
        if (Subscriber==self.name) and (entered_password == self.password):
            print(f'{self.name} authenticated')
        else:
            print('please check and enter valid username and password')

#SignUp to a new supscriptionName

    def signUpsubscription_type(self, new_subscription_type):
        self.subscription_type = new_subscription_type
        print(f'{self.name} subscription upgraded: {new_subscription_type}')

#Customize preferences

    def personalizePreferences(self, new_category):
        self.preferences = new_preferences
        print(f'{self.name} preferences updated: {new_category}')

    def display(self):
        print(f'Name: {self.name}')
        print(f'Email: {self.email}')
        print(f'Birth Year: {self._birth_year}')
        print(f'Subscription Type: {self.subscription_type}')
        print(f'Category: {self.category}')

2- SUBSCRIPTION

#Define the subscription Class representing the Type of Subscription available e.g News letter, Digital Copy

class Subscription:
 
    def __init__(self, subscription_id, subscription_type, num_subscribers):
        self.subscription_id = subscription_id
        self.subscription_type = subscription_type
        self.num_subscribers = num_subscribers
        self.enrolled_subscribers = []

    def subSignup(self, subscriber):
        self.enrolled_subscribers.append(subscriber)
        print(f'{subscriber.name} subscribes to {self.subscription_type}')

    def display(self):
        print(f'Subscription ID: {self.subscription_id}')
        print(f'Subscription Name: {self.subscription_type}')
        print(f'Enrolled Subscribers: {", ".join([sub.name for sub in self.enrolled_subscribers])}')

  

3- ARTICLE

#Define  Article class to represent content to  post

class Article:

    def __init__(self, title, content, author, publication_date = 0):
        self.title = title
        self.content = content
        self.author = author
        self.publication_date = publication_date

    def submit(self, title, content):
        self.title = title
        self.content = content
        print('Submission Successfully Submitted on:')


    def review(self):
        if self.content:
            print(f'{self.title} Approved for Publication')


    def publish(self):
        self.content = True
        self.publication_date = input(f'{self.title} to be published on: ')

    def display(self):
        print(f'Article Title: {self.title}')
        print(f'Article Content: {self.content}')
        print(f'Article Author: {self.author}')
        print(f'Article Publication Date: {self.publication_date}')



# USAGE EXAMPLE

user1 = Subscriber('Funsho', 'funsho.layo@gmail.com', 2002,'Fn34@ln2', 'News Letter','Culture')
user2 = Subscriber('James', 'james.Mayor@gmail.com', 1994,'mes#yor5', 'Digital Copy','Sport')
user3 = Subscriber('Peju', 'peju_sexxy@gmail.com', 2000, 'sexxy_02', 'Digital Copy','LifeStyle')


sub1 = Subscription('MW01','News Letter', 1)
sub2 = Subscription('MW02','Digital Copy',2)



Artc1 = Article('My Surrogacy Thoughts', 'It is safe to say most women want to have children...', 'Khadijat Ojo', '4:6:2021')
Artc2 = Article('Excel Project Showcase', 'In evaluating the Excel project, the grading criteria as mentioned...', 'Kemi Kane', '10:12:2023')
Artc3 = Article('Matriarchy on Call', 'Ladi is wonder embodied in a petite kinetic frame. Swift, decisive and brash.', 'Salome Cole')



sub1.subSignup(user1)
sub1.subSignup(user2)
sub1.subSignup(user3)


Funsho subscribes to News Letter
James subscribes to News Letter
Peju subscribes to News Letter



sub2.subSignup(user2)
sub2.subSignup(user3)

James subscribes to Digital Copy
Peju subscribes to Digital Copy


user1.display()
user2.display()
user3.display()

Name: Funsho
Email: funsho.layo@gmail.com
Birth Year: 2002
Subscription Type: News Letter
Category: Culture

Name: James
Email: james.Mayor@gmail.com
Birth Year: 1994
Subscription Type: Digital Copy
Category: Sport

Name: Peju
Email: peju_sexxy@gmail.com
Birth Year: 2000
Subscription Type: Digital Copy
Category: LifeStyle


sub1.display()
sub2.display()

Subscription ID: MW01
Subscription Type: News Letter
Enrolled Subscribers: Funsho, James, Peju

Subscription ID: MW02
Subscription Type: Digital Copy
Enrolled Subscribers: James, Peju



Artc1.display()
Artc2.display()
Artc3.display()

Article Title: My Surrogacy Thoughts
Article Content: It is safe to say most women want to have children...
Article Author: Khadijat Ojo
Article Publication Date: 4:6:2021

Article Title: Excel Project Showcase
Article Content: In evaluating the Excel project, the grading criteria as mentioned...
Article Author: Kemi Kane
Article Publication Date: 10:12:2023

Article Title: Matriarchy on Call
Article Content: Ladi is wonder embodied in a petite kinetic frame. Swift, decisive and brash.
Article Author: Salome Cole
Article Publication Date: 0












