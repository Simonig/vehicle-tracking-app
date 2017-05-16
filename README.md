# Vehicle Tracking App

This App shows the current position of all the Vehicles.


* Ruby version: 2.4.0

* Rails version: 5.1.1

* To run the project on localhost on port 3000 just run in the project folder: 
    bundle install
    rake db:migrate
    rails server

* Services 

    Add Current Location:
    
    POST to "localhost:3000/api/v1/gps" with the following data structure:
 
        {   
           "latitude": -33.408104, //float
           "longitude": -70.583771, //float
           "vehicle_identifier": "hhww225", //string
           "sent_at": "2016-8-25 20:45:00" //datetime
        }
        
    It creates a new Position for the selected Vehicle by vehicle_identifier, 
    if there is no vehicle with the chosen identifier, creates a new vehicle.


