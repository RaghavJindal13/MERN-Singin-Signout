# MERN-Singin-Signout
####  How to run this code
1. Clone this repository
2. Open command line in the cloned folder,
   - To install dependencies, run ```  npm install  ``` or ``` yarn ```
   - To run the application for development, run ```  npm run development  ``` or ``` yarn development ```
3. Open [localhost:3000](http://localhost:3000/) in the browser
----
# tutorial notes
Sign up: Users can register by creating a new account using an email address.
User list: Any visitor can see a list of all registered users.
Authentication: Registered users can sign-in and sign-out.
Protected user profile: Only registered users can view individual user details after signing in.
Authorized user edit and delete: Only a registered and authenticated user can edit or remove their own user account details.



Babel
Since we will be using ES6+ and the latest JS features in the backend code, we will install and configure Babel modules to convert ES6+ into older versions of JS so that it's compatible with the Node version being used.
Webpack is a static module bundler for JavaScript applications — it takes all the code from your application and makes it usable in a web browser. ... When Webpack processes your application, it builds a dependency graph which maps out the modules that your project needs and generates one or more bundles
in our  case dist folder
Nodemon
To automatically restart the Node server as we update our code during development, we will use Nodemon to monitor the server code for changes. 


babel bana di -- install and add babelrc file 
webpack banaya--install and add 3 files
nodemon install--just install
config  
running script in packagwe.json development = nodemon

express:
install kar pehle to
mern-skeleton/server/express.js:
mern-skeleton/server/server.js:

With a Node- Express- and MongoDB- enabled server now running,

mern-skeleton/server/models/user.model.js:

The password string that's provided by the user is not stored directly in the user document. Instead, it is handled as a virtual field.
sab ho gaya password vagera

routes set karenge 
  create,
  userByID,
  read,
  list,
  remove,
  update 
see in  controller.js

abhi humne crud set kar diya ab karenge ki authenticated users hi kar payen ye backchodi

ab backend set ho gaya hai 
check karne ke liye postman 

In the backend, we implemented a user model for storing user data, implemented with Mongoose; user API endpoints to perform CRUD operations, which were implemented with Express; and user auth for protected routes, which was implemented with JWT and express-jwt.
We also set up the development flow by configuring Webpack so that it compiles ES6+ code using Babel. We also configured Nodemon so that it restarts the server when the code changes. Finally, we checked the implementation of the APIs using the Advanced Rest API Client extension app for Chrome. 

Now, ...

Adding a React Frontend to Complete MERN

Home page: A view that renders at the root URL to welcome users to the web application.
Sign-up page: A view with a form for user sign-up, allowing new users to create a user account and redirecting them to a sign-in page when successfully created.
Sign-in page: A view with a sign-in form that allows existing users to sign in so they have access to protected views and actions.
User list page: A view that fetches and shows a list of all the users in ...

Configuring Babel and webpack
update template.js and add script tag
This script tag will load our React frontend code in the browser when we visit the root URL '/' 

Core React modules: react and react-dom 
React Router modules: react-router and react-router-dom
Material-UI modules: @material-ui/core and @material-ui/icons

In the client/user/api-user.js file, we will add methods for accessing each of the user CRUD API endpoints, 

To manage auth state in the frontend of the application, the frontend needs to be able to store, retrieve, and delete the auth credentials that are received from the server on successful user sign in. In our MERN applications, we will use the browser's sessionsStorage as the storage option to store the JWT auth credentials. 

Alternatively, you can use localStorage instead of sessionStorage to store the JWT credentials. With sessionStorage, the user auth state will only be remembered in the current window tab. With localStorage, the user auth state will be remembered across tabs in a browser.

Currently, when the React Router routes or pathnames are directly entered in the browser address bar or when a view that is not at the root path is refreshed, the URL does not work. This happens because the server does not recognize the React Router routes we defined in the frontend. We have to implement basic server-side rendering on the backend so that the server is able to respond when it receives a request to a frontend route.

To render the relevant React components properly when the server receives requests to the frontend routes, we need to initially generate the React components on the server-side with regard to the React Router and Material-UI components, before the client-side JS is ready ...


