# lambda-sqs

In this application, I am using two lambdas with aws sqs service. Sqs is great for decoupling the application. In this application, Api will trigger a lambda which in turn send msg to sqs service. Sqs has a url to send the message to. I am using aws sdk to send msg to sqs with params containing msg and url. If error occurs it will return a 500 code else it returns Id of the message that was just created.

A second lambda get triggered when there is a message in the sqs.

testing:
curl -d '{"text" : "Hello world!"}' https://7hhxrjzzua.execute-api.us-east-1.amazonaws.com/dev/sender
