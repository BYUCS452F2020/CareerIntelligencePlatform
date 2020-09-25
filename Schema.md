### Schema


##### User 

    User ( 
        UserID, 
        UserName, 
        FirstName, 
        LastName, 
        Email, 
        SubscriberType
    )
    
    Foreign Key UserName references Credentials
    Table Explantion: Holds the data for each User.

    Columns:
        UserID: Unique identifier for each user.
        FirstName: User's first name.
        LastName: User's last name.
        Email: User's email address.
        SubscriberType: Paid or Free
	


##### Goal 


    Goal ( 
        UserID, 
        Title, 
        Description, 
        Duration, 
        Type,  
    )
    
    Foreign Key UserID references User 
    Table Explantion: Holds the data for each Goal.

    Columns:
        UserID: Unique identifier for owner.
        Title: Title of goal.
        Description: Description of goal
        Duration: duration of goal
        Type: Type of goal


##### PaymentInformation 
    
    PaymentInformation (
        PaymentID,
        UserID,
        PaymentType,
        CardNumber
    )
   
    Foreign Key UserID references User
    Table Explantion: Holds the payment details for users.
    
    Columns:
        PaymentID: Unique identifer for a payment
        UserID: Unique identifer referencing a user.
        PaymentType: Credit | Debit
        CardNumber: Number for the card the user used.
