### FishBrain Catches REST API

The goal of this project is to assess development skills suitable for a backend developer position. It tests knowledge and proficiency with software design, unit testing and web technologies like HTTP and REST.

- **Project Name:** Fishbrain Catches REST API
- **Project Goal:** Create a small web-app for uploading catches with photos
- **Technology:** Pick any language, web framework and testing framework you like (although we’d prefer to see Go, Ruby/Rails or Node.js using Javascript/CoffeeScript)
- **Deliverables:** The solution should be sent using the greenhouse.io link that will be provided during the interview process.

**Description:**

Users (also called anglers) can use the mobile app to add their catches. The mobile app uses a REST API to create catches. A catch has a photo and some other attributes. After a catch has been created a job is queued by the REST API to resize the photo into a size more suitable for the mobile app.

The mobile app also has a feed that shows all catches. For every catch the app requests and displays the associated photo.

**Task:** Build the REST API and background photo resizing described above. Write unit tests for each component.

**Requirements:**

1. Design your API in a RESTful way and respond with JSON.
1. Make sure your code has tests.
Write the code and design your system to be as realistic and production-ready as possible. Follow best-practices and focus on quality.
1. A catch should have the following attributes: name of angler, species, weight, length, latitude, longitude and a timestamp.
1. Add 3 endpoints:
 
  * **Create catch:**

    - Request: attributes for a catch including the photo as a [HTTP multipart/form-data upload](http://stackoverflow.com/questions/4238809/example-of-multipart-form-data).
    - Should parse input including file upload, save to database, enqueue background job and send response.
    - To keep things simple, no authentication needs to be performed. Instead the name of the angler can be sent in the request as a string.

  * **Get all catches:**

    - Should return all catches in the system ordered by date (newest first).
  
  * **Get resized photo for a catch**

1. Background job to resize photo:
  * All photos should be resized to be max 140x140px
1. Describe your solution in a README and how to run it.


**Guidelines**

Please commit often and with good commit messages. This will allow us to see how you've approached the problem. Don't worry about changing things around often.

Don’t hesitate to ask any questions if you’re uncertain about the task or anything else is unclear.

Some hints: For background processing you could use something like Resque/Sidekiq with Redis or channels if you’re using Go. To resize images you can use ImageMagick.


**What is this?**

This repo contains the job assignment for potential Backend engineers at Fishbrain, you can apply for a job at: jobs@fishbrain.com

