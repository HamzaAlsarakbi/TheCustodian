# AlAmeen Use Cases

## Case 1: Creating a plan

### Actor

User

### Flow

1. User opens the program
2. User clicks New Plan
3. User checks "Lock Plan"
4. User enters a password

## Case 2: Creating an Chequing Account

### Actor

User

### Flow

1. User clicks "New"
2. User clicks "Chequing Account"
3. User enters the name of the chequing account(Main)
4. User chooses the balance ($CAD)
5. User chooses leaves the "max balance" checkbox unchecked
6. User sets the starting balance as $0


### Altnernative Flow

1.1. User sets the starting balanvce as < $0

   1. Program shows error "Starting balance must be a non-negative number".

## Case 3: Creating a Savings Account

### Actor

User

## Flow

1. User clicks "New"
2. User clicks "Savings account"
3. User enters the name of the account
4. User selects Car as the savings type
5. User chooses the currency in the account (CAD)
6. User enters the starting balance for the savings account ($0)
7. User leaves the minimum balance unchecked
8. User checks the maximum balance
9. User sets $1000 as the maximum balance
10. User checks

## Case 4: Creating a Budget

### Actor

User

### Flow

1. User clicks "New"
2. User clicks "Budget"
3. User enters the name of the budget
4. User sets the limit of the budget ($1000)
5. User selects the currency
6. User selects the tags that account to the budget
7. User selects an interval (Month)
8. User enters 1 as the interval number

## Case 5: Creating a deposit

### Actor

User

### Flow

1. User clicks "New"
2. User clicks "Deposit"
3. User selects the account
4. User sets the amount ($1000)
5. User selects the vendor tag (MyCompany)
6. User selects other tags (Salary)
7. User writes the statement "Work Deposit"
8. User leaves the time for today
9. User clicks create

### Alternative flow

4.1. The amount currency doesn't match the account

  1. Display error "Amount and account currencies don't match"
  2. Highlight the amount currency
  3. Highlight the account

7.1. The account exceeds max balance and there is a savings account

  1. Send a notification that the money was deposited in a savings account

7.2. The account exceeds max balance and there is no savings account

  1. Deposit the amount
  2. Send a notification that the account exceeds the max balance

## Case 6: Creating a withdrawal

### Actor

User

### Flow

1. User clicks "New"
2. User clicks "Withdrawal"
3. User selects the account
4. User sets the amount ($1000)
5. User selects the vendor tag (Amazon)
6. User selects other tags (Online, Fashion)
7. User leaves the statement blank
8. User leaves the time for today
9. User clicks create

### Alternative Flow

7.1. Insufficient funds

1. Display error "Insufficient funds"
2. Highlight the amount
3. Highlight the account

## Case 7: Creating a Transfer

### Actor

User

### Flow

1. User clicks "New"
2. User clicks "Transfer"
3. User selects the account from
4. User selects the account to
5. User sets the amount ($1000)
6. User leaves the statement blank
7. User leaves the time for today
8. User clicks create

### Alternative Flow

5.1. Insufficient funds

1. Display error "Insufficient funds"
2. Highlight the amount in red
3. Highlight the account from in red

5.2. Max balance reached

1. Display error "Account [Account Name] will exceed the max balance"
2. Display option "Adjust amount to the max balance"
3. Highlight the amount in red
4. Highlight the account to in red
5. Disable create button until user fixes the issue

## Case 8: Creating Auto-Deposit

### Actor

User

### Flow

1. User clicks "New"
2. User clicks "Auto-Deposit"
3. User selects the account (Main)
4. User sets the amount ($100)
5. User sets the repeat policy (bi-weekly every friday)
6. User leaves the end repeat unchecked
7. User clicks "Create"

## Case 9: Creating Auto-Withdrawal

### Actor

User

### Flow

1. User clicks "New"
2. User clicks "Auto-Withdrawal"
3. User selects the account (Main)
4. User sets the amount ($100)
5. User sets the repeat policy (bi-weekly every friday)
6. User leaves the end repeat unchecked
7. User clicks "Create"

## Case 11: Insufficient Funds from Auto-Withdrawal

### Actor

System

### Flow

1. System attempts an automatic withdrawal
2. System fails
3. System pushes a notification to the user about the issue
