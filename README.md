Week 2 Workshop Assignment

Completion requirements
 Done: View  To do: Make a submission  To do: Receive a grade

 
What You'll Do

Demonstrate your ability to implement Mongoose Schemas and Models, and to use them to interact with the collections and documents in a MongoDB server.
This assignment will use MongoDB on your local machine for grading purposes.


Instructions

In this assignment, you will add Mongoose Schemas and Models for the partners and promotions data. You will also update the partnerRouter and promotionRouter to handle requests to their REST API endpoints by using the Mongoose Models. You will be working with files in the nucampsiteServer folder.


Task 1: Create a Schema and Model for Partners

Model module: In the nucampsiteServer/models folder, create a new file named partner.js.
Schema: In this file, create a new Mongoose Schema named partnerSchema. Use this sample partner document given below as your guide:
{
    "name": "Mongo Fly Shop",
    "image": "images/mongo-logo.png",
    "featured": false,
    "description": "Need a new fishing pole, a tacklebox, or flies of all kinds? Stop by Mongo Fly Shop."
}
Schema Fields: All fields should be required except for "featured", and the name should be unique.
Timestamps: Ensure that each document created from this Schema will automatically be given CreatedAt and UpdatedAt fields.
Model: Create a Model named Partner from this Schema.
Export: Export the Partner Model from this module.


Task 2: Create a Schema and Model for Promotions

Model module: In the nucampsiteServer/models folder, create a new file named promotion.js.
Schema: In this file, create a new Mongoose Schema named promotionSchema. Use this sample promotion document given below as your guide:
{
    "name": "Mountain Adventure",
    "image": "images/breadcrumb-trail.jpg",
    "featured": true,
    "cost": 1299,
    "description": "Book a 5-day mountain trek with a seasoned outdoor guide! Fly fishing equipment and lessons provided."
}

Schema Fields: All fields should be required except for "featured", and the name should be unique.

Timestamps: Ensure that each document created from this Schema will automatically be given CreatedAt and UpdatedAt fields.
Cost: Use the mongoose-currency library's Currency type for the cost field.
Model: Create a Model named Promotion from this Schema.
Export: Export the Promotion Model from this module.


Task 3: Update the routers

Updates: For both the partnerRouter and promotionRouter, update the response to each defined endpoint using the new Partner and Promotion Models, exactly as you did with the campsiteRouter in the final two exercises this week.
Test: Use Postman to test each of your updated endpoints and verify that you receive the expected responses. Don't forget your MongoDB server must be running.
Test GET/POST/PUT/DELETE requests to: /partners and /partners/:partnerId
For the POST request to /partners, make sure to send a JSON string in the body of the request. Use the sample partner document given in Task 1.
For the PUT request to /partners/:partnerId, make sure to send the same document, but with at least one field changed so that you can verify an update has been made.
Repeat the same steps for testing /promotions and /promotions/:promotionId endpoints, using the sample promotion document given in Task 2.


Submission

Submit a total of 5 files:
One zipped file of your entire nucampsiteServer folder, excluding the node_modules folder, with your updated files.
PLUS the following 4 files, uploaded individually:
partner.js
promotion.js
partnerRouter.js
promotionRouter.js
OR, a text file containing the link to a public online Git repository for your project.


Assignment Resources

Mongoose Schemas / Mongoose Models / Mongoose-currency
