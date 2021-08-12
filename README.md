# SMSTeknikClient



Step 1: 

`nuget Install-Package SMSTeknikClient`


Step 2: 

```
var client = SMSTeknikClient.CreateClient( myUserId, myUserPassword ); 
var msg = new SMSMessage 
{
   To = "+2134", 
   Text = "Hello, World!",
   // You can specify lots of other stuff here! See documentation for details. 
}; 

var response = await client.SendMsg(msg); 
// You can check for status, delivery reports, failure details etc on the response
