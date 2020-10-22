# Sable Coding Challenge

## Context

Imagine you're working as a programmer for Sable. The data team has just created an advanced model for flagging suspicious transactions from user to user. This model is still in the early stages, so they want to pass the transactions on for manual review. The challenge is to create a small full stack application for the fraud team that consists of a server and a web based UI in order to manage reported transactions.

## Requirements

The UI should look something like the below, suspicious transactions should be ordered from newest to oldest: 

![Coding Challenge](https://i.imgur.com/x7gBW35.png "UI")

We do not expect you to connect to a DB for this task, but instead please use an in-memory data structure on the backend (a simple JavaScript object is fine), and fill the appropriate fields in the wireframe

We need a way to allow and block transactions. The two buttons in the UI should do a call to your backend service in order to block the transaction or to allow it. You are free to implement this as you want.

- Block: Means that the transaction should be marked as blocked
- Allow: Means that the transaction is allowed
    
Both blocked and allowed transactions are considered resolved and are not visible to the fraud team - this status should persist between refreshes (F5) of the frontend

## Notes

- Please don't spend more than 3 hours on this
- Please use NodeJS and React/React Native to implement this. Bonus points for using Typescript and GraphQL - but please only use these technologies if you are familiar with them and can complete the challenge within the time limit
- Provide the solution source code as a link to the code repository - please provide invites to a private repo if you don't want it public

What we're looking for:

1. High code quality (you should favor quality over quantity)
2. Pragmatic technical choices
3. A runnable full-stack application
