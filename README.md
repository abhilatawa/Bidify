# BidX- Buy & Sell

Welcome to BidX, your online marketplace for buying and selling second-hand items through a dynamic and user-friendly bidding system. BidX is designed to bring together a community of buyers and sellers, offering a wide range of pre-owned items from electronics and books to furniture and collectibles. Our platform caters especially to students, providing an affordable and reliable way to purchase essentials and more.

- _Date Created_: 03 Feb 2024
- _Last Modification Date_: 12 April 2024

## Deployment

To deploy our Angular frontend on Netlify, we configure it for production optimization and manage build commands and redirects directly on the platform, ensuring API URLs are appropriately set in the environment settings.

1. Push "bidx-frontend" code to the remote branch (preferably Github).
2. Update [apiUrl](bidx-frontend/src/environment.stage.ts) with the deployed backend URL.
3. Update [environments.ts](bidx-frontend/src/environments/environment.ts) with your firebase configurations.
4. Go to [Netlify](https://www.netlify.com/) and click on "Add new site".
5. Select "Import an existing project" and then "Deploy with Github".
6. Choose the "bidx-frontend" repo pushed earlier.
7. Netlify will detect Angular repo and the "main" branch will be deployed.

For our Spring Boot backend on Render.com, we use Docker to maintain consistent operations, establish necessary environment secrets via the platform's dashboard, and activate automatic deployments upon new commits to streamline and ensure efficient deployment processes.

1. Push "bidx-backend" code to a remote branch (preferably Github).
2. Update [WebConfig](bidx-backend/src/main/java/com/example/bidxbackend/config/WebConfig.java) with the deployed frontend URL.
3. Update [FirebaseConfig](bidx-backend/src/main/java/com/example/bidxbackend/config/FirebaseConfig.java) with the sdk and other configurations.
4. Update [spring.data.mongodb.uri](bidx-backend/src/main/resources/application.properties) with your mongodb database connection url.
4. Go to [Render](https://render.com/) and click on "New Web Service".
5. Select "Build and deploy from a Git repository".
6. Choose the "bidx-backend" repo pushed earlier.
7. Render will detect Spring boot repo (picks up the main branch) and the "main" branch will be deployed.

## Built With

- [Angular](https://angular.io/): A TypeScript-based open-source web application framework for building client-side web applications.
- [Spring Boot Java](https://spring.io/projects/spring-boot): An open-source Java-based framework used to create standalone, production-grade Spring-based Applications.
- [npm](https://www.npmjs.com/): The package manager for JavaScript and the world's largest software registry.
- [Gradle](https://gradle.org/): An open-source build automation tool used for building, testing, and deploying software packages.
- [Material UI](https://material.angular.io/): A UI component library for Angular based on Google's Material Design.
- [Firebase](https://firebase.google.com/): A platform developed by Google for creating mobile and web applications.
- [GitHub](https://github.com/): A web-based platform for version control using Git.
- [Render](https://render.com/): Ideal for backend deployment. *Note: We have used Render to deploy the backend, so initially it might take some time to load.*
- [Docker](https://www.docker.com/): Used for deployment containerization.
- [Netlify](https://www.netlify.com/): Used for frontend deployment.

## Acknowledgements

Here in our web app, we have used the Image Slider on the home page and the images used there are created using [Canva](https://www.canva.com/).

We would like to acknowledge [Angular](https://angular.io/docs) documentation for the whole front-end code and [Material UI](https://material.angular.io/guide/getting-started) for providing the UI design for the header bar.

## License
This project is licensed under the MIT License - see the [LICENSE](LICENSE) file for details.
