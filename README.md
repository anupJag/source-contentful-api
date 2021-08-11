# source-contentful-api
Source System to manage data for other systems.

## How does the system work
This system acts as a source system for different web applications to manage their metadata. Web apps often have their own ways of managing this use case. Source-contentful allows to bring these requests into a single platform.

The application, uses built-in authorization and authentication using OAuth 2.0.

## Architecture

- Low latency
- High Availability
- Separation of Concern
- Headless Architecture

The system will be built using all Open Source Technologies.

### Backend

The backend uses Nest JS for building api's using decorator pattern. The core of the backend app is to have a slug based api which can be used to fetch the data from the database.
Api's are built under isolation from others allowing user to create as many endpoints as they require. (This will be currenly capped to a limited size which can be further extended).

The Sourceful content will allow user to register other systems, so that these are whitelisted and will allow to overcome CORS issue.

The data will be stored under policy and guidelines.

Data will be cached using Redis to create low latency throughput.

### Database Design and Decision

Since creating a structured data will incur problems with building out decisions - We will be using Mongo DB for unstructured data accumulation. The database will evolve with time and new decisions will be taken based on the structure is finalized.

### UI
As part of the UI, we will use React as the core library and Next JS to house API's builts. The Login Page and the Sign Up page will use Server Side Rendering so that the pages are crawled for visibility on Google Searches.

Login Page: 
The login page will contain 2 fields (UserName/Password) and a Log In Button.
The page will transmit the data via secured server built into Next JS. The password will be 

