# MRHB Coding Challenge

## Introduction

Thanks for your interest in joining the MRHB engineering team! Before we proceed with more
formal interviews, we ask that all candidates submit a coding challenge. The coding challenge is
a foundational piece of our process and it's referenced later in our process during the technical 
interviews.

If at any point you have questions concerning the coding challenge and/or interview process, please
do not hesitate to reach out to your point of contact via email.

## Coding Challenge

The coding challenge revolves around building a task list. Tasks belong to groups and can have
dependencies on one another (i.e. if task X depends on task Y, task X cannot be completed until
task Y is completed). The challenge includes 3 components:

* Build React-based UI
* Complete a backend interface
* Design database schema
* Implement Web3 Wallet Connection (preferably MetaMask or WalletConnect)

### Build React-based UI

The UI consists of 2 screens:

* **Overview**: Displays a list of all the groups along with their completion status. Clicking on 
  a group should render the detail screen.

* **Detail**: Displays a list of all the tasks in the selected group and allows the user to toggle 
  the completion status of unlocked tasks.

The screens should look like this:

![screen design](https://user-images.githubusercontent.com/314351/56453206-d1ec2580-62f3-11e9-83d7-67aff2e1deef.png)

The data you should use to implement your solution is available at a `GQL Query` called `tasks`, you can find it on _./client/src/graphql/getTasks.graphql_.
SVG assets for the icons used in the design live in _./client/public/_.

Some things to keep in mind:

* Locked tasks cannot have their completion status toggled
* Tasks remain locked until all of their dependencies have been completed
* When clicking the box to complete a task, you must use the `toggleTask` mutation. 
* Your implementation should resemble the above design
* We value well structured code that follows best practices

### Complete a backend interface

As mentioned above, you will need to use the `toggleTask` mutation to complete/un-complete a task. To accomplish this, you will need to implement the backend logic for toggling the task.

### Design Database Schema

Design a schema in SQL to store the task list data. You can add the SQL code needed to create
the schema to _schema.sql_. The schema should define all tables, columns, and constraints needed
to store the task list data.

### Implement Web3 Wallet

A user should be able to connect their MetaMask wallet to the app and app should load tasks for that specific user. You can use Metamask Wallet Address to identify the user, as this is unique public key that only that specific user has access to.

## Getting Started

- To get started, clone this repo to your local machine.
- Next you'll want to install the dependencies and run the client and server (we recommend using `node: v14.15.4`):

    ```bash
    cd server
    yarn install
    yarn dev
   ```
   open other terminal on the root of this project
   ```bash
   cd client
   yarn install
   yarn start
   ```

At this point, the client and server should be running in development mode and any local modifications you make
will be automatically detected and result in reloads.

You should only need to add/modify code in the _./client/src/_ and _./server/src/_ directory.

## Submission

To submit your coding challenge, take following steps:

```
# Create your branch based off main branch in format like so:
submissions/name-surname-date

# Commit your code to your branch and notify your point of contact when it is complete
```

Thanks for taking the time to do this coding challenge and here's hoping we talk soon!