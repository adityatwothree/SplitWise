Well, a lot have used splitwise (Atleast sharing people). havent we!.SO this is an expense sharing application.

An expense sharing application is where you can add your expenses and split it among different people. 
The app keeps balances between people as in who owes how much to whom.

## Example
```
You live with 3 other friends.
You: User1 (id: u1)
Flatmates: User2 (u2), User3 (u3), User4 (u4)

This month's electricity bill was Rs. 1000.
Now you can just go to the app and add that you paid 1000,
select all the 4 people and then select split equally.
Input: u1 1000 4 u1 u2 u3 u4 EQUAL

For this transaction, everyone owes 250 to User1.
The app will update the balances in each of the profiles accordingly.

User2 owes User1: 250 (0+250)
User3 owes User1: 250 (0+250)
User4 owes User1: 250 (0+250)
---


Now, It is the BBD sale on Flipkart and there is an offer on your card.
You buy a few stuffs for User2 and User3 as they asked you to.
The total amount for each person is different.
Input: u1 1250 2 u2 u3 EXACT 370 880

For this transaction, User2 owes 370 to User1 and User3 owes 880 to User1.

The app will update the balances in each of the profiles accordingly.
User2 owes User1: 620 (250+370)
User3 owes User1: 1130 (250+880)
User4 owes User1: 250 (250+0)

---

Now, you go out with your flatmates and take your brother/sister along with you.
User4 pays and everyone splits equally. You owe for 2 people.
Input: u4 1200 4 u1 u2 u3 u4 PERCENT 40 20 20 20

For this transaction, User1 owes 480 to User4, User2 owes 240 to User4 and User3 owes 240 to User4.

The app will update the balances in each of the profiles accordingly.
User1 owes User4: 230 (250-480)
User2 owes User1: 620 (620+0)
User2 owes User4: 240 (0+240)
User3 owes User1: 1130 (1130+0)
User3 owes User4: 240 (0+240)
    
```

## Input
1. All inputs will be taken from STDIN.
2. There will be 3 types of input:

1. New Users Addion: ``` ADD <no-of-users> <space-separated-list-of-user-names>```. The ID will be incremental in the form of ``` u1, u2, u3, u4... ```
2. Expense in the format: ``` EXPENSE <user-id-of-person-who-paid> <no-of-users> <space-separated-list-of-user-ids> <EQUAL/EXACT/PERCENT> <space-separated-values-in-case-of-non-equal> ```
3. Show balances for all: ``` SHOW ```
4. Show balances for a single user: ``` SHOW <user-id> ```
