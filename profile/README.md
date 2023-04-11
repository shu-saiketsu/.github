# Saiketsu Voting Project 【採決】 さいけつ

<img align="right" width=300px  src="https://media3.giphy.com/media/kAnRgAnE5KuDUHtXNc/giphy.gif?cid=ecf05e47643daqgoivc2hrlksvh9v9j0ky61wshjosl6awuw&rid=giphy.gif&ct=g" />

## 👨🏻‍💻 About the Project

The project's name is taken from the Japanese word ['to vote'](https://jisho.org/word/%E6%8E%A1%E6%B1%BA). **Why?** Because I learned Japanese for a week, and I want to make sure all that knowledge I learned is shown off in style. 😎

The project is **microservice based** and allows users to vote in elections and allows the creation of elections using administrator accounts. 

The project you see is in its **final submission** as it was when it was submitted on the **27th April 2023** at **15:00 GMT**. Do not use this project in production applications due to its lack of updates, there may be severe security vulnerabilities present.

💡 Centralised voting system based on the microservice architecture.\
🪥 Uses CQRS to allow independent scaling.\
🫧 Integrates with the [Clean Architecture](https://github.com/jasontaylordev/CleanArchitecture) to provide seperation.\
🎓 Implements an API gateway to abstract away microservices.\
🌱 Uses Auth0's Authentication and RBAC systems to securely verify actions.\
🔥 Implements RabbitMQ to ensure eventual consistency is met.\
✅ Uses different voting systems for a variety of environments.\
✍️ Created as a disertation project for Sheffield Hallam University.\
🕒 **TODO: UPDATE MARK HERE WHEN DONE**

## 🛠 Tech Stack

All the technology, and utilities, that were used to make this project a success.

![Auth0](https://img.shields.io/badge/-Auth0-05122A?style=flat&logo=auth0)
![Swagger](https://img.shields.io/badge/-Swagger-05122A?style=flat&logo=swagger)
![Git](https://img.shields.io/badge/-Git-05122A?style=flat&logo=git)
![GitHub](https://img.shields.io/badge/-GitHub-05122A?style=flat&logo=github)
![Markdown](https://img.shields.io/badge/-Markdown-05122A?style=flat&logo=markdown)
![Visual Studio Code](https://img.shields.io/badge/-Visual%20Studio%20Code-05122A?style=flat&logo=visual-studio-code)\
![Visual Studio](https://img.shields.io/badge/-Visual%20Studio-05122A?style=flat&logo=visual-studio)
![RabbitMQ](https://img.shields.io/badge/-RabbitMQ-05122A?style=flat&logo=rabbitmq)
![PostgreSQL](https://img.shields.io/badge/-PostgreSQL-05122A?style=flat&logo=postgresql)
![Docker](https://img.shields.io/badge/-Docker-05122A?style=flat&logo=docker)
![TypeScript](https://img.shields.io/badge/-TypeScript-05122A?style=flat&logo=typescript)\
![Eslint](https://img.shields.io/badge/-ESLint-05122A?style=flat&logo=eslint)
![Prettier](https://img.shields.io/badge/-Prettier-05122A?style=flat&logo=prettier)
![React](https://img.shields.io/badge/-React-05122A?style=flat&logo=react)
![NextJs](https://img.shields.io/badge/-NextJS-05122A?style=flat&logo=next.js)
![Mui](https://img.shields.io/badge/-MUI-05122A?style=flat&logo=mui)
![HTML](https://img.shields.io/badge/-HTML-05122A?style=flat&logo=HTML5)
![CSS](https://img.shields.io/badge/-CSS-05122A?style=flat&logo=CSS3)\
![.ENV](https://img.shields.io/badge/-.ENV-05122A?style=flat&logo=.env)
![C#](https://img.shields.io/badge/-CSharp-05122A?style=flat&logo=Csharp)
![ReSharper](https://img.shields.io/badge/-ReSharper-05122A?style=flat&logo=resharper)
![DataGrip](https://img.shields.io/badge/-DataGrip-05122A?style=flat&logo=datagrip)
![GitHub Actions](https://img.shields.io/badge/-GitHub%20Actions-05122A?style=flat&logo=github-actions)\
![React Hook Form](https://img.shields.io/badge/-React%20Hook%20Form-05122A?style=flat&logo=react-hook-form)
![Windows Terminal](https://img.shields.io/badge/-Windows%20Terminal-05122A?style=flat&logo=windows-terminal)
![Spotify](https://img.shields.io/badge/-Spotify-05122A?style=flat&logo=spotify)
![YouTube](https://img.shields.io/badge/-YouTube-05122A?style=flat&logo=youtube)\
![StackOverflow](https://img.shields.io/badge/-StackOverflow-05122A?style=flat&logo=stackoverflow)
![Google](https://img.shields.io/badge/-Google-05122A?style=flat&logo=google)
![Microsoft Teams](https://img.shields.io/badge/-Microsoft%20Teams-05122A?style=flat&logo=microsoft-teams)
![Postman](https://img.shields.io/badge/-Postman-05122A?style=flat&logo=postman)
![.NET](https://img.shields.io/badge/-.NET-05122A?style=flat&logo=.net)\
![JetBrains](https://img.shields.io/badge/-JetBrains-05122A?style=flat&logo=jetbrains)
![Discord](https://img.shields.io/badge/-Discord-05122A?style=flat&logo=discord)
![Mozilla](https://img.shields.io/badge/-Mozilla-05122A?style=flat&logo=mozilla)
![Google Chrome](https://img.shields.io/badge/-Google%20Chrome-05122A?style=flat&logo=google-chrome)
![Giphy](https://img.shields.io/badge/-Giphy-05122A?style=flat&logo=giphy)
![JSON](https://img.shields.io/badge/-JSON-05122A?style=flat&logo=json)

## ⚙️ Installation and Configuration
Each microservice is isolated, meaning that it does not reply upon other microservices to function.

- Please see each different service's **README.md** for further instructions.
- External services such as Auth0 are not covered.

## 🥅 Microservices
There are a total of five **(5)** microservices in the solution. In addition, there is also a **gateway** and **frontend** application.

### 🤺 Gateway
Utilises CQRS to independently CRUD data from resources (micro-services). Uses Auth0 as an authorization, authentication and RBAC source to protect endpoints.

### 🔥 Frontend
Communicates with the gateway to perform CRUD actions upon the user. Connects with Auth0 to provide login and cookie functionality.

### 👤 Candidate Service
Provides a source of truth for candidate entities in the system.

### 📃 Vote Service
Provides a source of truth for vote entities in the system.

### ⚡ Election Service
Provides a source of truth for election entities in the system. A large aggregator of entities in the system as it uses many integration events to sync entities together.

### ✅ User Service
Provides a gateway for the Auth0 implementation.

### 🥳 Party Service
Provides a source of truth for party entities in the system.

## 💖 Acknowledgements

Special thanks to these folks for making the process and project possible!
- **(Project Supervisor)** Dr. Soumya Sankar Basu
- **(External Examiner)** Dr Kathy Clawson
- Sheffield Hallam University
- Friends, family and StackOverflow
- Dancing Cat GIFs

<div align="center">
  <sub>Voting is, and should remain an essential part of democracy.</sub>

  <sub>Made with 💖 by <a href="https://github.com/whatshark">Nathan Hall</a>.</sub>

  <img height="30" src="https://cdn3.emoji.gg/emojis/6021_Cat.gif">
</div>




