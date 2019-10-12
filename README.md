# lambda-sqs

In this application we are using two lambdas with aws sqs service. Sqs is great for decoupling the application. In this application Api will trigger lambda which in turn send msg to sqs service. Sqs has a url to which we send the message to. we will use aws sdk to send msg to sqs with params containing msg and url. If error occurs we will return a 500 code else we will return Id of the message we just created.

A second lambda get triggered when there is a message in the sqs.

testing:

curl -d '{"text" : "Hello world!"}' https://7hhxrjzzua.execute-api.us-east-1.amazonaws.com/dev/sender
