## Final Screencaptures of Client

![alt text](https://github.com/defiantgoat/woowoofund-design/blob/main/campaign-view.png)
![alt text](https://github.com/defiantgoat/woowoofund-design/blob/main/manage.png)
![alt text](https://github.com/defiantgoat/woowoofund-design/blob/main/create.png)

---

## Project Requirements
 
The Challenge

Build a tool that allows a user to upload their pitch deck and display it on a web page.
At a minimum, you should have:
A web page that allows a user to upload a file as a PDF. Bonus points for supporting PPT and other formats too.
A backend that takes the uploaded file and generates an image for each slide.
A web page that displays the deck using the image of each slide, like on the Wefunder profile page.
 
You don't have to worry about user accounts or supporting multiple company profile pages. It's OK if the display page simply shows the last deck that was uploaded to the upload page.
 
You can use any technology stack, libraries, and APIs you're comfortable with. The design/architecture is up to you. The UI can be basic, but should look halfway good.
 
Commit your project to a git repo and push it to GitHub. Include a README file that explains how to run your project. It should work on a Ubuntu 20 machine.
## Tech Overview
### [Front-End Client](https://github.com/defiantgoat/woowoofund-app)
* React based web application
* Will run with a small ExpressJS server application inside a docker container
* Will authenticate and have a JWT that will be used for api related requests.
* This is the view to the models/controllers based in the separate api. The client is dumb.
* Runs in a docker container in k8s, AWS ECS or some similar cloud environment.
#### POC Notes
* For POC the client’s state will load with a simulated authenticated user with a mock JWT.
### [Back-End API](https://github.com/defiantgoat/woowoofund-api)

* Standards based endpoints
* Uses JWT for authentication required transactions.
* Runs in a docker container in k8s, AWS ECS or some similar cloud environment.
#### Technology Stack
##### Option 1
* Ruby/Sinatra based backend API with ActiveRecord ORM
##### Option 2
* Express JS based backend API with sequelize ORM.
#### POC Notes
* For POC, database interactions will be simulated. So ORM will not be implemented.




