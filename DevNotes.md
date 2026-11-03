Oliver Warlick's Dev Notes
## Step 1: Identify Conditions and Actions

Review the reservation requirements and identify:

- Five conditions that affect whether a reservation is accepted.:

1-The check-in date is before the checkout date. 
2-Payment is successful. 
3-Payment fails. 
4-Current date matches the check-in date.
5-The reservation is currently in a Pending or Confirmed state. 


- Five actions that may occur based on those conditions.:

1-Add the one-time $50 cleaning fee. 
2-Move reservation state to Confirmed.
3-Move reservation state to Cancelled.
4-Move reservation state to Checked In. 
5-Raise an InvalidStateError. 


## Step 2: Create a Decision Table

Create a decision table containing at least six relevant combinations of conditions and their expected actions.

Use:

- `T` for true
- `F` for false
- `-` when the condition does not affect the result
- `X` when an action should occur

Your table should follow this structure:

| Conditions and Actions         | Rule 1 | Rule 2 | Rule 3 | Rule 4 | Rule 5 | Rule 6 |
| ------------------------------ | :----: | :----: | :----: | :----: | :----: | :----: |
| Dates are valid                |        |        |        |        |        |        |
| Number of nights is valid      |        |        |        |        |        |        |
| Number of guests is valid      |        |        |        |        |        |        |
| Requested nights are available |        |        |        |        |        |        |
| More than five guests          |        |        |        |        |        |        |
| **Create reservation**         |        |        |        |        |        |        |
| **Calculate standard price**   |        |        |        |        |        |        |
| **Add extra guest fee**        |        |        |        |        |        |        |
| **Raise `ValueError`**         |        |        |        |        |        |        |
| **Raise `UnavailableError`**   |        |        |        |        |        |        |

`See decision table and tests.xlsx`

## Step 3: Create Decision Table Test Cases

Create at least one test case for every rule in your decision table. If your table contains six rules, you must create at least six test cases.

Each test case must include:

- Test-case ID
- Conditions
- Input values
- Expected action
- Expected price or exception

`See decision table and tests.xlsx`

## Step 4: Identify Reservation States and Events

- Identify five possible reservation states.
- Identify five events that may cause the reservation to change states.

### Reservation States

- `Pending`
- `Confirmed`
- `Checked In`
- `Completed`
- `Cancelled`

### Events That Change Reservation States

- Payment succeeds
- Payment fails
- Guest checks in
- Guest checks out
- Guest / system cancels reservation


</details>

## Step 5: Create a State Transition Table

Document the expected result of each event from each relevant state.

Your table must include at least:

- Six valid state transitions
- Three invalid state transitions
- Nine transitions total

Use the following structure:

| Current State | Event            | Expected State | Expected Result          |
| ------------- | ---------------- | -------------- | ------------------------ |
| Pending       | Payment succeeds | Confirmed      | Reservation is confirmed |
|               |                  |                |                          |

`See State Transition Table and test cases.xlsx `

## Step 6: Create State Transition Test Cases

Create test cases that cover:

- Every valid state transition, for a minimum of six test cases
- At least three invalid state transitions
- At least one complete reservation sequence
- At least one cancellation sequence

You must create at least 11 state transition test cases in total.

`See State Transition Table and test cases.xlsx`

## What to Submit

1. Create and initialize a GitHub repository.
2. Commit and push your work to the repository.
3. Make sure the repository is public. Private repositories will not receive credit.
4. Submit the repository URL on Canvas.

## AI Transparency

AI was used in the creation of this file.
