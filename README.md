## Project Requirements

When a founder is looking to raise capital for their company, a fair amount of thought will go in to their pitch deck. They will share their deck with potential investors to help sell investors on why they should invest in the company.
We want to make raising money on Wefunder as simple as possible, so we allow founders who have already built a pitch deck to upload it to Wefunder and we'll show their deck on their profile — rather than forcing the founder to recreate their pitch on our site.
 
You can see an example of this on Wefunder's own company profile (we dogfood our own product to raise our rounds): https://wefunder.com/wefunder
 
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




