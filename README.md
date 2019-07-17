**1.**  **Assignment 4:**
    
    The following features have been developed as part of the fourth assignment:
        
        1. Checkout Services: This features provides a receipt to the customers about the details of his order and the amount that he has paid
        for that order.The receipt is emailed to the user as an attachment.
        
        2. Payments System: This feature allows the users to pay for the services that they have purchased.The user can fill all the mandatory 
        details and pay for the services.
            
        The url for the payments system and checkout services is mentioned below:
        
        http://bluenose.cs.dal.ca:35826/checkout
            
        Since both the services are interlinked.Therefore, these both services cover the three features of the application which are Payment System,
        Receipt Generation and Email System which were presented during the Project Proposal.
            
            
**2.**  **Libraries Used**

        The following libraries have been used to develop the backend of the above mentioned features:
        
        1.  react-stripe-checkout - This library provides the default payment system.It can be used in test mode and the development mode.
            For this application, we are using this in test mode as we need to build a dummy payment system.
            
        2.  receipt - This library provides the layout to create a receipt.This receipt will be used to notify the user about his order details.
        
        3.  nodemailer - This library has been used to create the email server.
        
**3.** **How to use the application**

        1. Download the project from the below mentioned repository:
        
        
        
**3.**  **Coding References**

        1. Modified Code:
           
           var receiptOutput = receipt.create([{
                type: 'text',
                value: [
                    'Book It',
                    'Thanks for supporting Local!',
                    ]     
           
           Reference Code:
           
           const output = receipt.create([
                { type: 'text', value: [
                    'MY AWESOME STORE',
                    '123 STORE ST', 
                    ]
                }
            
            Reference:
            Receipt. Retrieved from https://www.npmjs.com/package/receipt
            
            This reference has been used to create the receipt for the customer as per the requirement.
          
        2. Modified Code:
        
            await transporter.sendMail({
                from: 'singh.manpreet4664@gmail.com',
                to: request.body.email,
                subject: "Your Order Receipt",
                text: receiptOutput,
      
        
           Reference Code:
           
           const mailOptions = {
                from: "nicklaus.roach@gmail.com",
                to: "nicklaus.roach@gmail.com",
                subject: "Node.js Email with Secure OAuth",
                generateTextFromHTML: true,
                html: "<b>test</b>"
            };
           
           Reference:
           (2019, June 04). Sending Emails with Node.js Using SMTP, Gmail, and OAuth2. 
           Retrieved from https://medium.com/@nickroach_50526/sending-emails-with-node-js-using-smtp-gmail-and-oauth2-316fe9c790a1
           
           This tutorial has been used to create the email server.
           
        3. Modified Code:
        
           setTimeout(function () {
            window.location.reload();
            }, 3000);
            
           Reference Code:
           
           window.location.reload(true);
        
           Reference:
           FreeCodeCamp. Location Reload Method. Retrieved from https://guide.freecodecamp.org/javascript/location-reload-method/
           
        