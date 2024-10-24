# ECom-Services

I developed a comprehensive e-commerce service API featuring several key components: a product service for inventory management and a secure authentication service for user logins. To manage traffic efficiently, I implemented an API gateway for load balancing and used Eureka for seamless service discovery among microservices. The payment service is integrated with Razorpay, enabling secure transactions. Additionally, an email service leverages Kafka to listen for events and automatically send notifications to users. This architecture enhances scalability and provides a smooth user experience across the platform.

Authentication service
githubRepo: https://github.com/ramya24-eng/EComUserService
Host URL: http://user-service-latest-env-1.eu-north-1.elasticbeanstalk.com/login (temporarily instance was stopped)
About: I developed an authorization server to facilitate secure user login and protect the resource server, specifically the product service, from unauthorized access. This server ensures that only authenticated users can retrieve data from the product service. Each API call requires a valid token, which is validated against the authorization server to confirm user identity and permissions. By implementing this token-based access control, the system effectively safeguards sensitive information while enhancing user security and maintaining a seamless experience for authenticated users.
hosted sign up page 
![image](https://github.com/user-attachments/assets/6f05437a-5cd9-4ef4-96ba-f6b38858ff21)

Given a authorization details to authenticate and generate token 
![Screenshot 2024-10-24 132124](https://github.com/user-attachments/assets/e7657271-8f86-42c4-bb7b-7518943bc34f)

On login 
![Screenshot 2024-10-24 132344](https://github.com/user-attachments/assets/3d2109d0-574f-4019-b26d-f45d8925f424)

Authorization consent check to generate token
![Screenshot 2024-10-24 132427](https://github.com/user-attachments/assets/f0a216d5-010a-4ef1-bc0a-6a15a67905ad)

Generated token sucessfully
![Screenshot 2024-10-24 132541](https://github.com/user-attachments/assets/20c4bb12-2e3a-41c3-a5f7-b0b1e2ee0b1a)

Used a MYSQL Database hosted in AWS RDS to store user details
![image](https://github.com/user-attachments/assets/ee3810f2-7859-4725-baa6-ef4ca97d4397)


Product service 
github Repo: https://github.com/ramya24-eng/EComProductService
Host URL: http://ecomproductservice-env.eu-north-1.elasticbeanstalk.com/products/1 (temporarily instance was stopped)
About: I developed an API that supports CRUD operations for effective resource management. Utilizing RestTemplate, the API retrieves sample data from external sources, ensuring seamless integration. I also implemented robust exception handling to gracefully manage errors during data operations. This approach provides informative responses to clients while maintaining system stability.

Rendering data on hosted url based on custom call
![image](https://github.com/user-attachments/assets/db6b9de8-6ad3-499c-9548-471cbc09dd8d)

Apigateway service
githubRepo:https://github.com/ramya24-eng/EcomAPIGateway
About: I created an API gateway service that registers with Eureka for service discovery and enables load balancing. This gateway efficiently redirects incoming API calls to the appropriate backend services. By managing traffic and enhancing reliability, it streamlines communication between clients and services. Overall, this architecture improves system performance and scalability.

ServiceDiscovery Service
githubRepo:https://github.com/ramya24-eng/EcomServiceDiscovery
About: I utilized Eureka as a service discovery mechanism to enable dynamic communication between microservices within the application. By registering each service with Eureka, I ensured that they could locate and interact with one another without hardcoded endpoints. This approach simplifies scaling and managing service instances, as Eureka automatically updates the registry with the current state of available services. Overall, it enhances system resilience and facilitates seamless integration across the microservices architecture.
Gateway get registered in eureka
![image](https://github.com/user-attachments/assets/a3193e0d-5326-40a1-a2c5-c46b0b00ab37)


Payment Service
githubRepo:https://github.com/ramya24-eng/EComPaymentService
About: I implemented a payment gateway using Razorpay to facilitate secure and seamless transactions for users. This integration allows for various payment methods, including credit/debit cards, net banking, and digital wallets, enhancing user convenience. I also ensured robust error handling and transaction validation to maintain security and reliability. Overall, this solution provides a smooth payment experience while safeguarding user data.

Email Service
githubRepo:https://github.com/ramya24-eng/EComEmailService
About: I implemented real-time email notifications for user sign-ups by leveraging Kafka for event-driven messaging. When a user completes the registration process, an event is published to a Kafka topic, triggering the email service to send a verification email promptly. This approach ensures timely communication and improves user engagement during the onboarding process. Additionally, the use of Kafka enhances scalability and reliability in handling email notifications.





  

