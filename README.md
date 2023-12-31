# Image Search App Using React

This project is built using Vite which is a popular alternative to `create-react-app`.

By building this app, I learned:
- How to build an application using Unsplash API in React
- How to make API Calls in different scenarios
- How to use `useCallback` hook to avoid function re-creation
- How to use ESLint to fix application issues
- How to Implement Pagination in React

## Project Setup

1. Clone the Repository to your local machine using ZIP File or using the following git command:
```
git clone https://github.com/aniru-dh21/Image_Search.git
```

2. Install the dependencies using `npm`:
```
npm install
```

3. Run the command to access the application:
```
npm run dev
```

4. Access the application by navigating to <ins>http://127.0.0.1:5173/</ins>

## How to Get Access to the Unsplash API

- Now, to implement the image search, we need to get the API key from <a href="https://unsplash.com/">Unsplash Website</a>.

- Navigate to <a href="https://unsplash.com/developers">this URL</a>, and click on the "Register as a developer" button displayed at the top right corner of the page.

- Create your account by entering all the necessary details.

- Once registered, you will be redirected to <a href="https://unsplash.com/oauth/applications">this page</a>.

- Click on the `New Application` button. On the next screen:
  - Check all the checkboxes and click on `Accept Terms` button
  - Enter values for `Application name` and `Description` and click `Create application` button.

- Scroll down a bit and copy the Access Key which is displayed on the screen.

- Next, create a new `.env` file in your project and add a new environment variable with the name `VITE_API_KEY`.

- Also, assign the copied value of the API key to it:
```
VITE_API_KEY=367ykb9dWL9AlAIAsK9Sz2ga8t5xPNeYFcf70xwCGbA
```

- Make sure to start the variable name with `VITE_` so it will be accessible in the application.

- Now, navigate to <a href="https://unsplash.com/documentation">Unsplash Documentation</a> and click on the `Search photos by keyword` section.

- And copy the following base API URL: `https://api.unsplash.com/search/photos`.

- Now, open `App.jsx` file and paste the copied URL as `API_URL` after all import statement, like this:
```
const API_URL = 'https://api.unsplash.com/search/photos';
```

- According to the documentation, the search photos API with the above URL accepts the `query`, `page` and `per_page` as the query parameters.
