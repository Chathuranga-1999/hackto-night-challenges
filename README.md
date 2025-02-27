# hackto-night-challenges
Hakto-night hackathon challenges

Wireframe Link 
https://teamnsbm.invisionapp.com/freehand/HackToNight-wgwePXDwf?dsid_h=55dc1f16be3f1faf0bb2ea991f2efb1fd3254fc20c8861434ae56b6c25332746&uid_h=0ec8f7954c539782cd817636ab96a70c400f6f6501495d8d7e8132c7335ecbb1

Problem Scenario 

 BBH Warehouse is an import and export company. They do buy and sell in their local area as well.
BBH warehouse has a computer-based system for online customers, and it allows their users to log into their system. The users can browse items, make purchases, and place their orders just like they usually do in a regular shopping application.
There are some government rules that regulate the minimum amount of money a buyer can spend when buying items in bulk. A buyer’s annual income should be approximately 1 million rupees for purchasing or placing an order from the BBH warehouse. When a user places an order from the BBH warehouse system the company must have 50% of the requested product more, left in stock. For example, if a customer requests to buy 100 candies, the seller must have at least 150 candies in their stock to sell 100 to the customer. If the BBH warehouse doesn't hold 50% more of the requested product in stock, they won’t be able to sell due to the market rules and regulations.
This system has a user end also an admin end. It fulfils the basic CRUD Operations (CREATE, READ, UPDATE, DELETE). There is a login space that both users and admins can use to log in to the system. The admins can update data about the products and advertisements and edit them or delete them if there is no need. Additionally, users are able to give feedback on a product as a comment on the product itself 

 

 

Use the following  

 

User Login 

payload 

 { 

 
	

"username": self.username, 

 
	

 
	

 "email": self.email, 
	

 "password": self.password 

 
	

 
	

        } 

 

Endpoint 

api/register 

response schema 

{ 
	

    "$schema": "http://json-schema.org/draft-04/schema#", 
	

    "type": "object", 
	

    "properties": { 
	

        "email": { 
	

            "type": "string" 
	

        }, 
	

        "role": { 
	

            "type": "string" 
	

        }, 
	

        "user_id": { 
	

            "type": "integer" 
	

        }, 
	

        "username": { 
	

            "type": "string" 
	

        } 
	

    }, 
	

    "required": [ 
	

        "email", 
	

        "role", 
	

        "user_id", 
	

        "username" 
	

    ] 
	

} 

Check login 

 

{ 
	

        "email": self.email, 
	

        "password": self.password 
	

    } 

 

Endpoint 

api/login 

 

Schema 

{ 
	

  "$schema": "http://json-schema.org/draft-04/schema#", 
	

  "type": "array", 
	

  "items": [ 
	

    { 
	

      "type": "object", 
	

      "properties": { 
	

        "feedback_id": { 
	

          "type": "integer" 
	

        }, 
	

        "feedback": { 
	

          "type": "string" 
	

        }, 
	

        "user": { 
	

          "type": "integer" 
	

        } 
	

      }, 
	

      "required": [ 
	

        "feedback_id", 
	

        "feedback", 
	

        "user" 
	

      ] 
	

    } 
	

  ] 
	

} 
	

 
	

create_feedback_list = { 
	

  "$schema": "http://json-schema.org/draft-04/schema#", 
	

  "type": "object", 
	

  "properties": { 
	

    "feedback": { 
	

      "type": "string" 
	

    }, 
	

    "feedback_id": { 
	

      "type": "integer" 
	

    }, 
	

    "user": { 
	

      "type": "integer" 
	

    } 
	

  }, 
	

  "required": [ 
	

    "feedback", 
	

    "feedback_id", 
	

    "user" 
	

  ] 
	

} 
	

 
	

 
	

login_response_schema = { 
	

  "$schema": "http://json-schema.org/draft-04/schema#", 
	

  "type": "object", 
	

  "properties": { 
	

    "auth_token": { 
	

      "type": "string" 	

    } 
	

  }, 
	

  "required": [ 

    "auth_token" 

 } 

 

Feedback 

{ 
	

  "$schema": "http://json-schema.org/draft-04/schema#", 
	

  "type": "array", 
	

  "items": [ 
	

    { 
	

      "type": "object", 
	
      "properties": { 
	

        "feedback_id": { 
	
          "type": "integer" 

        }, 
	

        "feedback": { 
	

          "type": "string" 1
        }, 
	
        "user": { 
          "type": "integer" 
        } 
      }, 

      "required": [ 
        "feedback_id", 
        "feedback", 
        "user" 
      ] 
	
    } 
	
  ] 
} 
	

create_feedback_list = { 
	
  "$schema": "http://json-schema.org/draft-04/schema#", 
  "type": "object", 
  "properties": { 
    "feedback": { 
	

      "type": "string" 
    }, 
	

    "feedback_id": { 
      "type": "integer" 

    }, 
	
    "user": { 
      "type": "integer" 
    } 
	
  }, 
	
  "required": [ 
    "feedback", 
    "feedback_id", 
    "user" 
	
  ] 
	
} 
