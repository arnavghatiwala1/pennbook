# pennbook
## A Miniature Facebook

### TEAM MEMBERS

   Madelyn Dempsey: dmadelyn, 
   Nick Kuo: nickkuo, 
   Alan Du: ydu24, 
   Arnav Ghatiwala: arnavg

### FEATURE DESCRIPTIONS

        Login:
            On the login page (the default page), users can enter a username and password, which triggers a call to our backend to see if the password was correct, and makes use of our encryption scheme to ensure that passwords are hashed correctly. 

        User Registration:
            User registration (reachable via the /register route or when someone clicks create account from the login page) shows the user 8 input fields to enter their information in order to register. The user must enter a unique username, a password, first name, last name, email, at least two interests (selected via a dropdown with pre-set inputs that the user can choose from), affiliation, and birthday. The interests are restricted to a certain subset of interests in order support the 
            newsfeed feature properly. If the user fails to fill in a field or choose at least two interests, then an error message will pop up and the user info will not be written to our database. 

        Visualizer:
            The graph icon take the user to the /visualizer page where first themselves as the center node shows up with direct conenctions to each of their immediate friends. Then, bu clicking a friend the graph expands to add that person's friends filtered for those with the same affiliation as the current user. 

        Account Changes:
            A user can press an icon in their navigation bar that routes them to /editprofile where they can make changes to their email, affiliation, password, and interests. Again, the interests input field requires at least two inputs, or else the user will see an error message and the updates will not be made in the backend, so no post request is made. Each input field triggers a different action, so only one change can be made at a time. This page also displays the UserInfo component, so the user can see their current information. 

        Navigation Bar:
            At any point after logging in, a user can see a navigation bar displayed at the top of their screen. In this navbar, there is a search bar, and several icons to route the user to different features within the application:

        Search Bar: 
            As the user types a name into the search bar, a dropdown of suggested users is displayed based on the users in our database whose first and last names start with the letters typed by the user. For instance, if a user types s and Sarah Batta and Steph Cao are users in the system, then Sarah Batta and Steph Cao will be displayed under the search bar. This bar is not case-sensitive, and once a suggestion or the search bar has been pressed, the user will be routed to that person's profile page, provided that they are in the system. 

        Edit Profile Icon:
            Once the user pressed the icon in the navbar with a box surrounding a person icon, they will be redirected to /editprofile and the account changes feature, as described above. 

        NewsFeed Icon:
            When a user presses the NewsFeed icon (image of a newspaper) they will be redirected to our newsFeed via the /newsfeed route, where their personalized feed will be displayed. 

        Chat Icon:
            When the user presses the chat icon (a message bubble) they will be redirected to their personal chat page via the /chat route. 

        Logout Icon:
            When the user presses the logout icon (door with arrow) they will be logged out, the session will be cleared so that their username is no longer available in the cookies, and and they will be redirected to the login page. 

        Home Icon: 
            When the user presses the home icon (house) they will be redirected to their personal home page containing their post feed, account overview, and profile via the /home route. 

        Graph icon: 
            takes the user the the visualizer 

        Home Page:
            When the user lands on their home page (/home) they will see their feed of posts 

        User Profiles:
            By clicking the photo icon in the header the user is routed to /profile/user where they can see thier wall, panel of freinds and their current login status, account overview, and commenting ability. 
        
        Chat:
            by clicking the chat button they are brought to the chat screen where the left panel shows friends and their login status as well as any current invites. Then the middle panel shows the current conversations and where notifications for new chats will come up, and the user can actually send messages in the right panel. 

        NewsFeed:
                The news button in the header takes the user to the news page where they will see a search bar to search for keywords in articles, and their recommended article based on adsorption. After searching for a word or words, they will see a list of news similar to the feed structure where they can like posts, and the posts are ordered in relevance to the users (by number of keywords that are present from the search query and by adsorption score)

### EXTRA CREDIT
    - infinite scrolling on the home and profile pages. 

### SOURCE FILES
    All application-related files will be found in FinalProject:
        backend folder:

        routes 
            - routes.js : has all of the routes to our backend - all of the routes that our frontend calls for dynamodb queries
        models
            - database.js : contains the logic for our dynamo db calls and routes

        nets212 folder:

        src
        - components
            - chat : all necessary files for the chat component
                - Chat.css
                - Chat.jsx
                - ChatBox.css
                - ChatBox.jsx
                - ChatListItem.css
                - ChatListItem.jsx
                - ChatMessageItem.css
                - ChatMessageItem.jsx
                - FriendListItem.css
                - FriendListItem.jsx
                - InviteListItem.css
                - InviteListItem.jsx
            - editAccountFold : style and code for the edit account page, uses userinfo component as well
                - EditAccount.css
                - EditAccount.jsx
            - FriendPanelFold : code and style for panel showing a user???s friends and login status which is used on the profile page
                - FriendPanel.css
                - FriendPanel.jsx
            - header : style and code for header - has search bar for users and icons to navigate the app
                - Header.css
                - Header.jsx
            - HomeFold : style and code for the home page
                - Home.css
                - Home.jsx
                - Wall.jsx
            - LoginFold : style and code for the login page
                - Login.css
                - Login.jsx
            - NewsFeedFold : style and code for news feed page, and the news component which styles and formats each individual news post
                - News.css
                - News.jsx
                - NewsFeed.css
                - NewsFeed.jsx
            - SignUpFold : style and code for the signup page 
                - Signup.css
                - Signup.jsx
            - UserInfoFold : style and logic for a dynamic card that shows the user???s current account info
                - UserInfo.css
                - UserInfo.jsx
            - visualizer : code for the visualizer componentn
                - Visualizer.jsx
        - comment.css
        - commen.jsx - code and formatting for comments on a post /page
        - Post.css - style and code for each individual post on a wall or home page
        - Post.jss
        - ProfilePage.css - style and code for a user???s profile page
        - ProfilePage.jsx
        - SharePost.css - style and code for sharing a post
        - SharePost.jsx
        - App.js : contains the main routes for the frontend of the project

### INTEGRITY STATEMENT

    All code written in this project was written by one of the people listed in section 1), all code is original and developed for use in this project only. 

### INSTRUCTIONS
    To run our project, first start the backend server so cd into FinalProject/backend and run node app.js

    Then create a new terminal and cd into FinalProject/nets212 and run npm start

    The app is now available at localhost/3000 
