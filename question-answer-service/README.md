Question and Answer service

This service uses Mongodb to store the questions. It follows the following data model.

Question{
questionId:integer,
question: string,
description:string,
topics:list<string>,
upvotes:integer
timestamp:long
downvote:integer,
userDTO:{
     firstname:string,
     emailaddress:string,
     imageurl:string
     },
comments:[
	  {
	   comment:string,
	   timestamp:long,
	   likes:integer,
           userDTO:{
                 firstname:string,
                 emailaddress:string,
                 imageurl:string
                },
	   replies:[
		    {
		    reply:string,
		    likes:integer,
		    timestamp:long,
                    userDTO:{
                          firstname:string,
                          emailaddress:string,
                          imageurl:string
                         },
		     }
		   ],
	  }
	],
answers:[
	  {
	   answerDTO:string,
           accepted:boolean,
	   upvotes:integer,
	   views:integer,
	   timestamp:long,
           userDTO:{
                firstname:string,
                emailaddress:string,
                imageurl:string
                }
	   comments:[
		     {
			comment:string,
			timestamp:long,
			likes:integer,
                        userDTO:{
                             firstname:string,
                             emailaddress:string,
                             imageurl:string
                             }
			replies:[
				 {
				   reply:string,
				   likes:integer,
				   timestamp:long,
                                   userDTO:{
                                        firstname:string,
                                        emailaddress:string,
                                        imageurl:string
                                        }
				 }
				],
		     }
		    ],
	  }
	],
}