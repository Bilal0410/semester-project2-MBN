# React + Vite

This template provides a minimal setup to get React working in Vite with HMR and some ESLint rules.

Currently, two official plugins are available:

- [@vitejs/plugin-react](https://github.com/vitejs/vite-plugin-react/blob/main/packages/plugin-react/README.md) uses [Babel](https://babeljs.io/) for Fast Refresh
- [@vitejs/plugin-react-swc](https://github.com/vitejs/vite-plugin-react-swc) uses [SWC](https://swc.rs/) for Fast Refresh

Report:
Semester Project 2

This website is built using Vite and React with JavaScript. Vite is a fast build tool for web development, offering quick start-up times and efficient builds. Rwact is used for creating dynamic user interfaces. To get started, make sure you have Vite installed, and explore the JavaScript-written React components for a responsive web experience.

For this semester project the brief was to make an auction site where users can add items to be bid on and bid on items other users have put up for auction. When a new user joins through registering and logging in for the website, they are given 1000 credits to use on the site. They can get credits by selling items and use credit by buying items. Non-registered users can search through the listings, but only registered users can make bids on listings. For this project I used the Noroff Api documentation to be able to make all fetches.

For the HomePage a component is used called `AllListings` It helps users view, search, and add bid on auction listings. React hooks like `useState` is used to manage the components state and `useEffect` to fetch data from an external API. The `searchQuery` stores user input for searching through listings and filters listings based on title and description. The UI is simple and user-friendly for this page. Success and error messages display for when bidding or trying to bid for better user-experience.

For this website, users have to register an account first by filling in their name, email, password, and an avatar field with an image url. The registration form checks for valid inputs in real-time and gives feedback on successful registration. After signing up, users are automatically redirected to the login page. To access their personalized profile, users then log in using their registered email and password. The login process communicates with the server, handling potential errors like wrong passwords or non-existing username with clear messages. Once logged in successfully, users can view their profile page, which displays their name, chosen avatar, and credits. The application is designed to be user-friendly, with loading indicators and success messages for a smoother experience from registration to profile access. To be able to change avatar the user can easily click on the avatar image inside the ProfilePage and then place the new image url to be able to change the avatar. Users name, credits and avatar will always show on the navbar after registration and logging in. When a user bids on an item, the user should be able to see that credit being removed from his total credit.

The CreateListing component does the job of helping users add new listings easily. It keeps track of the listing details like title, description, tags, media URLs, and the end date using the `useState` hook. If users make mistakes while filling out the form, the component shows them errors in real-time so they can fix them on the spot. Notably, the code includes a date validation mechanism, ensuring that the specified end date is in the future within a reasonable timeframe. Media URLs are validated for correctness using a regular expression. Upon successful input and validation, the component sends a POST request to the server, creating a new listing. The user receives feedback in the form of success or error messages, contributing to a user-friendly experience. The form also prevents submission if errors are present, displaying a collective error message for user guidance. Overall this component is crucial for users to contribute content to the platform by adding new listings.

After successfully creating a listing, the user can go to the listing page and see the listing made next to other users listings. An error message will occur when user tries to bid on listings made by the user or other listing which has a bid amount higher than what the user tries to bid. To be able to see all the listings made by the user you can go to the profile page and find them there.

In this collection of React code snippets, the application comes to life with a seamless user experience. The `ProfilePage` component serves as the users hub, displaying their details and auction listings. It skillfully retrieves user data from local storage and communicates with the server to fetch and present their listings. The `LoginForm` and `RegisterForm` components handle user authentication, ensuring a secure and smooth onboarding process. User can register, log in, and subsequently access their personalized `ProfilePage`. Additionally, the `CreateListing` component let users to effortlessly contribute new listings, implementing real-time validation and feedback. Together, these components weave a friendly and well connected web application, providing users with a fluid journey from registration to listing creation and interaction with their profile. The code displays thoughtful consideration for user interactions, data validation, and effective communication with the server, resulting in a well-rounded and user-friendly application.

Sources and links:

Noroff API Documentation - https://docs.noroff.dev/

Figma link - https://www.figma.com/file/uJAeLdhiXNEgLnqq5gZJUd/Semester-Project-2?type=design&node-id=0%3A1&mode=design&t=kinIBZNTfy3eR0xR-1

Github link - https://github.com/Bilal0410/semester-project2-MBN

Netlify link - https://effulgent-marzipan-101baa.netlify.app/
