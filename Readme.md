# SendGrid Scheduler

REST API for scheduling mails with Sendgrid API using Node.js and Express.js framework with DiskDB.

A Job Scheduler that tasks up emails to be sent in future with a timestamp as input.
Also added support for template engine of SendGrid Console.

## Running project

You need to have Node.js installed.

### 1) Install dependencies 

To install dependencies enter project folder and run following command:
```
npm install
```

### 2) Run server

To run server execute:
```
npm start
```

### EndPoints

| HTTP METHOD | METHOD                      
| ----------- | --------------- | --------- | ----------- | ------ |
| /schedule     | GET        
| /schedule/:scheduleId       | GET 
| /schedule/create/  | POST |

### Inputs

| NAME | INFO | REQUIRED |                     
| ----------- | --------------- | --------- | ----------- | ------ |
| apiKey     | SendGrid API Key |Yes|        
| to       | Receiver's email | Yes| 
| from       | Sender's email | Yes| 
| subject       | Email Subject | Yes| 
| scheduleAt      | Timestamp when mail should be sent e.g 1411820580000  | Yes| 

#### For Standard Mails
| NAME | INFO | REQUIRED (any one) |                     
| ----------- | --------------- | --------- | ----------- | ------ |
| text     | Email Text/Contents | *|        
| html     | Email Html Contents | *|        

#### For Template Mails
| NAME | INFO | REQUIRED |                     
| ----------- | --------------- | --------- | ----------- | ------ |
| template_id     | Your SendGrid Template Id |Yes|  
| substitution name 1.     | E.g -name- |No|   
| substitution name 1.     | E.g -address- |No|   
| and so on     |  |No|   


## Author

This module was created by Karan K


## License

MIT
