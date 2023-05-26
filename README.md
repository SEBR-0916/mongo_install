## SEIR 0508

# MongoDB Installation Walkthrough

## What is a Database?

A database is an organized collection of data, stored and accessed electronically.  There are many kinds of databases. A common type is a RDBMS (relational database management system).  Relational databases are frequently based on SQL (Structured Query Language)  and store data in tables and rows, much like an Excel spreadsheet/Google Sheet.

Another type of database is a NoSQL database, which don't store data in rows and columns.  In this unit, we'll be using MongoDB which is a very popular NoSQL database for building web applications, and in particular, building web applications that need to store a lot of data.

## What is Mongo?

MongoDB is a specific type of NoSQL database system called a  **document database**.  It stores data in a format called BSON, which is a JSON-like format. One of the key benefit of this format is that it is very easy to work with using JavaScript because it so closely resembles plain old JavaScript objects!

MongoDB is also much more scalable than relational databases due to this mechanism of data storage.  It means that we can store the data easily across many physical pieces of hardware since each "record", is a separate and distinct "document".



MongoDB is a fantastic, internationally used database system. We will be using it through our second unit.

##  Installing and setting up MongoDB on MacOS.

First of all, a prerequisite for MongoDB install is that our command line tools are up to date. To make sure, run:

```sh
xcode-select --install
```

xcode is a LARGE file, somewhere around 10gb in size. Like mp3 downloads in the late 90's, you may see the Install Time start up in Hours, Days, or even Years. Usually that is just the engine warming up, and the install should only be around 10-15 minutes, if you don't already have it installed. If after 15-20 minutes it has not yet finished installing, or it still has the Time Remaining over an hour or so, restart your computer and try this step again. If this happens multiple times, please message one of your instructors and we will help you out when we return to class

Now for MongoDB. In our terminal, enter the commands:

```sh
brew tap mongodb/brew
```

This will install of the necessary dependencies for the Mongo system

Then we need to install the MongoDB Community Service...

```sh
brew install mongodb-community
```

Finally, we need to start up the service we just installed...

```sh
brew services start mongodb-community
```

Now if we run `brew services list`. You should see `mongodb-community` with the green word "started" to the right of it. Yay!

##  Linux/Ubuntu issues...

If you are getting any permission errors, simply add the Sudo (Super User Do) command before

```sh
sudo apt brew install mongo mongodb-community
```

If you got any errors there, please let your instructor know. Otherwise, you can verify that MongoDB is working correctly by running one of the following commands:

Now run `sudo systemctl status mongodb`. You should see a green circle and the words "active (running)" somewhere in the output.

## Running the Mongo Shell

If the service appears to be running, type `mongosh` and hit enter.

You should see something like this:

```
MongoDB shell version v4.2.0
connecting to: mongodb://127.0.0.1:27017
MongoDB server version: 4.2.0
```

The may be followed by some warnings/errors. Ignore these warnings/errors for now.
You should notice that your command prompt is gone, replaced with a `>`.
This means the MongoDB shell installed correctly. Press `Ctrl + c` to get back
to your terminal.

If there are any further errors, we may have to run

```sh
sudo apt update

sudo apt install -y mongodb
```

Please let your instructor know if you need to run these additional commands.

## MongoDB Databases, Collections and Documents

MongoDB is an application that runs as a **server** and can have many separate databases within it.

Each MongoDB **database** consists of collections.

Each **collection** is a set of documents.

Each **document** contains a set of data and attributes, known as fields.

However, in order to really use Mongo with deploying and sharing our data, we will need to sign up for a (free) account with what is called the MongoDB Atlas
[MongoDB Atlas](https://www.mongodb.com/cloud/atlas/register)

[Atlas Install Github Repo](https://github.com/SEIR-0508/u2_mongo_atlas_setup/blob/main/README.md)

If you are having trouble with this step, we will have some time allotted when we return this week to aid in installs and set up.

Once we have Mongo installed, and an account set up with Atlas, we can begin our journey into back end/server side coding next week.

## Windows Install

### Downloading the Client

First we need to download the community version of MongoDB, additional information and resources can be found in the link below

[Install MongoDB Community Edition on Windows](https://www.mongodb.com/docs/manual/tutorial/install-mongodb-on-windows/#install-mongodb-community-edition-on-windows)

Following the instructions in the link above, we can find the download for Mongo at

[MongoDB Community Download](https://www.mongodb.com/try/download/community)

![Screenshot 2023-05-26 081426](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/40eb43dc-3ef2-44c1-88ca-260ae1a8096f)

Make sure that you have the current version and the right platform and download the package and run it

![Screenshot 2023-05-26 081815](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/f2a79575-92e3-4edc-a707-d73d14ea64c6)

Click next, then accept terms and click next

After agreeing to the terms of service you'll be met by this screen, click complete

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/e4bff5f8-d5fb-48de-be30-c8b906e7d733)

Use the specs seen below 

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/2c5d18a2-86b0-42c6-a69b-0efc81a7cccb)

Click next, then install

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/286b18ac-c977-42ab-88f1-c37d305262d3)

It will load a downloading screen

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/e1b8b976-abd9-48c8-a614-101b8ba3331e)

When completed it will open Mongo Compass

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/65c15276-fac9-4645-8e40-ad596d5a3d86)

### Donwloading MonGosh

Mongosh allows us to test our Mongo code locally, we'll be using it to learn Mongo in our first few Mongo lessons, and later we will use it for debugging our apps

To download the install package, additional information and resources can be found in the link below

[Install mongosh](https://www.mongodb.com/try/download/shell)

Following the instructions in the link above, we can find the download for Mongosh below

[MongoDB Shell Download](https://www.mongodb.com/try/download/shell)

Mongosh only downloads as a zip, so you will have to extract it to it's own folder

After extracting the file we need to add it to our PATH

Open the Control Panel.

In the System and Security category, click System.

Click Advanced system settings. The System Properties modal displays.

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/7dbb94df-e962-42ed-bdfb-94391fc1af90)

Click Environment Variables.

In the System variables section, select Path and click Edit. The Edit environment variable modal displays.

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/b4cb7803-7191-47b3-ab7c-68f255665245)

Copy your mongo bin filepath

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/3832731b-0930-44dc-a474-14390bea582b)

Click New and add the filepath to your mongosh binary.

![image](https://github.com/SEIR-0508/u2_lesson_mongo_install/assets/100214696/8fca2244-c0bb-4676-9dfa-526811c97d61)

Click OK to confirm your changes. On each other modal, click OK to confirm your changes.

To confirm that your PATH environment variable is correctly configured to find mongosh, open a command prompt and enter the mongosh --help command. If your PATH is configured correctly, a list of valid commands displays.




