# Awesome Bank API Interaction with React and TypeScript

## Phase 1: Overview
This live coding session demonstrates how to build a React application with TypeScript to interact with the Awesome Bank API. We'll cover fetching and displaying user data and transactions, with a focus on handling pagination and errors.

Link with credentials and endpoint

https://awesome-bank.xyz/step-2-sleepy-euler.html

- GET https://awesome-bank.xyz/api/use
- GET https://awesome-bank.xyz/api/transactions?from={from}&limit={limit}


## Prerequisites
- Basic understanding of React and TypeScript
- Familiarity with REST APIs and async operations in React

## Setup
Fork the provided CodeSandbox template: [transactions-qpfqpz](https://codesandbox.io/p/sandbox/transactions-qpfqpz)

## Access Token
We will use the following hardcoded access token for this session:
`eyJ0eXAiOiJKV1QiLCJhbGciOiJIUzI1NiJ9.eyJzdWIiOiJkZTllMDhkMy03OWMyLTRjYjMtOTZmMi0wMjNmZWE3ODcyY2UiLCJpc3MiOiJhd2Vzb21lLWJhbmsifQ.4J1IAK7lFM8FWpO_y3vC-cTWkEIs3DGrNysaJSaS-IE`

## Key Concepts
1. **Fetching Data**: How to use Axios or Fetch API in a React TypeScript environment to get data from the API.
2. **Displaying Data**: Techniques to effectively display the user data and transactions in the UI.
3. **Error Handling**: Strategies for dealing with API instability and HTTP errors (e.g., HTTP 429).
4. **Pagination**: Implementing a "Load More" functionality for transaction data.

## Steps
1. **Setting Up the Project**: Overview of the existing CodeSandbox template structure.
2. **Creating API Service**: Setting up the API calls to fetch user data and transactions.
3. **Building Components**: Developing React components to display the data.
4. **Implementing Pagination**: Adding logic to handle loading more transactions.
5. **Error Handling**: Implementing error handling mechanisms for the API calls.

## Conclusion
Wrap-up and recap of what we've built. Discuss potential improvements or additional features.

## Phase 2: Implementing Pagination for Transactions

Useful link with resources:

https://awesome-bank.xyz/step-2-sleepy-euler.html

OR:

- GET https://awesome-bank.xyz/api/transactions?from={from}&limit={limit} (same token used above)

### Overview
In this phase, we will enhance our application by adding pagination to the transactions API call. This will allow us to load transactions in increments, rather than all at once, improving the performance and user experience.

### Objectives
1. Implement pagination logic to load transactions in batches.
2. Handle potential API errors and instabilities.

### Key Concepts
- **Pagination Parameters**: Understanding the use of `from` and `limit` query parameters in API requests.
- **State Management**: Managing the state for pagination (like the last transaction timestamp).
- **UI Interaction**: Updating the UI to allow users to load more transactions.

### Implementation Steps

1. **Update State for Pagination**:
    - Add state variables to keep track of the last transaction timestamp and whether there are more transactions to load.

2. **Modify API Call**:
    - Adjust the existing API call function to accept `from` and `limit` parameters.
    - Ensure that the function updates the state with the new transactions and the timestamp of the last transaction fetched.

3. **Add 'Load More' Button**:
    - Implement a button in the UI that, when clicked, triggers the fetching of more transactions using the updated API function.
    - The button should only be visible if there are more transactions to load.

4. **Error Handling**:
    - Implement error handling for the API request to manage HTTP 429 errors or other instabilities.
    - Display appropriate messages to the user in case of an error.

5. **Testing**:
    - Test the pagination feature to ensure it loads more transactions correctly and handles errors as expected.

### Expected Outcome
By the end of this phase, the application will be able to load transactions in a paginated manner. Users will be able to click on a 'Load More' button to load additional transactions. The application will handle API errors gracefully, providing a better user experience.

### Additional Notes
- Consider setting a reasonable default value for the `limit` parameter to balance load times and user experience.
- Ensure the UI is responsive during the loading of additional transactions and displays loading indicators appropriately.
