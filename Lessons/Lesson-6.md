# FEW 2.9 GraphQL and React

## 

- After Class/In classs activity
	- https://www.howtographql.com/react-apollo/0-introduction/
	- You can check your work agains the completed to tutorial here if you run into a problem: 
		- https://github.com/howtographql/react-apollo
- hackernews-react-apollo tutorial notes
	- Pay close atttention to the tutorial code snippets. The highlighted changes are not always correct! 
		- Stretch goal: make a pull request on the soruce repo for the tutorial if you see a mistake!
	- You'll be running two separate node projects from within the hackernews-react-apollo folder
		- in the root folder it will be the react project
		- in server folder will be the express server
	- Some instructions will ask you to switch folders in the terminal!
	- To run `yarn dev` in the *server* folder and launch the react app you'll need two terminals
	- Getting Started > Exploring the server
		- When you get here the tutorial asks you to run some commends to create some new posts. For this to work you'll need to be logged in and authorized. Create a user (if you haven't already)
```graphql
mutation {
  signup(email:"test@test.com", password:"test", name:"test") {
    user {
      name
      id
    }
  }
}
```
Now log in to this user account: 
```graphql
mutation {
  login(email:"test@test.com", password:"test") {
    user {
      name
    }
    token
  }
}
```
Copy the token and add the following to the HTTP Headers tab (lower left)
```graphql
{
  "Authorization":" Bearer <paste-token-here>"
}
```

	- Mutations: Creating Links > Writing the Mutation
		- I ran into a  problem here: `Unhandled Rejection (Error): Argument id for data.postedBy.connect.id must not be null. Please use undefined instead.` I'm guessing this is becuase you're not logged in and can't provide a user id which seems to be required for the database. 
		- I didn't find a good solution to allow posts without authenticating, and this is really the behavior that we want, for now I skipped the errors and continued with the tutorial. 
	

<!-- > -->


## After Class 

Time to start working on the frontend of hacker news!

Start working on the React + Apollo tutorial: <https://www.howtographql.com/react-apollo/0-introduction/>

- Complete the following chapters by next class: `Introduction`, `Getting Started`, `Queries: Loading Links`
















# Apollo

Apollo is a client that works with GraphQL. It can send requests and receive responses from a GraphQL endpoint. 

Apollo also has a library of React components that make it easy to integrate with React front ends. 

## Getting started 

Add Apollo to a React front end. 

- Import dependencies 
	- npm install --save graphql apollo-boost react-apollo graphql-tag

## In Class 

Review the tutorial. Look at its features and requirements. 


## Bonus Lesson: React Hooks!

Using state with functional components 

`const [state, setState] = useState(defaultValue)`