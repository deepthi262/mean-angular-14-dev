NodeJs/express JS flow
Require express, cors
Create app (Express application). The express() function is a top-level function exported by the express module.
Set corsOptions
app.use  
•	cors, 
•	express.json() :   parse requests of content-type - application/json
•	express.urlencoded : parse requests of content-type - application/x-www-form-urlencoded
require app/models
	require config ( mongodb connection url)
	require mongoose (nodejs module)
create db object : 	
o	mongoose,
o	url(above config url),
o	tutorials(model we define schema, method,  
mongoose.Schema, schema.method, mongoose.model  we are adding the schema to tutorial.
Mongoose.connect   create a promise for checking that connection(.then, .catch)
Creating simple route 	App.get
Require routes 
	Require tutorial controller
		Require models(same as above)
		Db.tutorials also from model
		Define methods for 
Create and Save a new Tutorial

	validate(from req body, check if title is empty),
	Create(use req.body to create new tutorial ) and 
	save tutorial (using  save(mongoose) , .then,    .catchsend result,status
			Retrieve all Tutorials from the database
				findAll get title (from req.query) and then frame condition
Tutorial.find  use condition from above, now with promise send result (.then, .catch)
			Find a single Tutorial with an id
				findOne method, get id from req, params
				Tutorial.findByID

			Update a Tutorial by the id in the request
				Validate req.body for empty
				Get the id from params and Tutorial.findByIdAndUpdate
			Delete by id, delete all is similar
Find all published Tutorials
		Require express.Router()
			Create post, get, put, delete, then app.use
	Define port and do app.listen at the given port



	

