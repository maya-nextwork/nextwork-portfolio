<img src="https://cdn.prod.website-files.com/677c400686e724409a5a7409/6790ad949cf622dc8dcd9fe4_nextwork-logo-leather.svg" alt="NextWork" width="300" />

# Save User Info with a Lex Chatbot

**Project Link:** [View Project](http://learn.nextwork.org/projects/aws-ai-lex4)

**Author:** Maya Menon  
**Email:** maya@nextwork.org

---

## Save User Info with a Lex Chatbot

![Image](http://learn.nextwork.org/cheerful_blue_peaceful_miromiro/uploads/aws-ai-lex4_505be5b8)

---

## Introducing Today's Project!

### What is Amazon Lex?

Amazon Lex is a AWS service and it is useful because it allows you to create chatbots without too much coding.

### How I used Amazon Lex in this project

In today's project, I used Amazon Lex to build a bot from scratch that greets the user, provide friendly error messages and returns a random bank balance when the user provides the account type and date of birth. The bot also remembers the date of birth for a period of time allowing the user to ask for other bank balance amounts without having to verify the user's date of birth again and again.

### One thing I didn't expect in this project was...

One thing I didn't expect in this project was how easy it is to change the duration of the bot's memory.

### This project took me...

This project took me less than 2 hours including creating the bot from scratch and creating this documentation.

---

## Context Tags

Context tags are like sticky notes that the bot keeps between intents. 

There are two types of context tags. We can set up an output context to store info after an intent is completed or an input context to check for info before an intent is triggered.ntext tags:...

I created a context tag called contextCheckBalance. This context tag was created in the intent CheckBalance. This tag stores information about our user's data of birth

![Image](http://learn.nextwork.org/cheerful_blue_peaceful_miromiro/uploads/aws-ai-lex4_97dc2351)

---

## FollowUpCheckBalance

I created a new intent called FollowupCheckBalance. The purpose of this intent is to allow users to ask a follow up question about another account balance.

This intent is connected to the previous intent I made, CheckBalance, because it performs the same function (return a random number for the bank balance when the account type and date of birth is provided). 

![Image](http://learn.nextwork.org/cheerful_blue_peaceful_miromiro/uploads/aws-ai-lex4_12345678)

---

## Input Context Tag

I created an input context, contextCheckBalance, that remembers the date of birth of the user before the FollowupCheckBalance.

![Image](http://learn.nextwork.org/cheerful_blue_peaceful_miromiro/uploads/aws-ai-lex4_c4fc89af)

---

## The final result!

To see the context tags and followup intent in action, I had to first trigger the CheckBalance intent by entering the input "check my balance," which resulted in a random bank balance. I then had to ask the question, "what about checking," in order to trigger the FollowupCheckBalance.

If I had gone straight to trying to trigger FollowUpCheckBalance without setting up any context, I would received a prompt from BankerBot asking for my verification details (date of birth). By setting up the context, BankerBot did not ask me for my date of birth again when I asked to check the balance of another account.

![Image](http://learn.nextwork.org/cheerful_blue_peaceful_miromiro/uploads/aws-ai-lex4_505be5b8)

---

## Managing context expiry

An extension for this project is to manage contextCheckBalance's context expiry, which means that we can set the number of times the bot will remember the user info or the amount of time before it forgets the user info. By default, expiry is in 5 turns or 90 seconds.

I updated my bot's context expiry to 2 turns or 10 seconds. What this means for my end users is that they can ask for a follow up bank balance request for 2 more times or within 10 seconds.

A long context expiry window would be helpful when we want the bot to remember our user's information for a longer conversation. A shorter context expiry window would be helpful when we want to a more secured conversation especially when sharing sensitve data.

![Image](http://learn.nextwork.org/cheerful_blue_peaceful_miromiro/uploads/aws-ai-lex4_81b763822)

---

---
