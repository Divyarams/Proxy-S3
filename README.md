# Proxy-S3
Accessing S3 resources using API GW Proxy without Lambda.

# Overview
Stage 1 : Create a rule in EventBridge by pattern matching for Object Creation in S3 and use Lambda as Target.
Stage 2 : Configure Lambda to recieve the event trigger and send ses email to user- with contents of body (bucket name and key)
Stage 3 : Verify reciever e-mail id in Sandbox mode in SES.
Stage 4 : API GW request and response defined for Resource - GET method. Use Path Parameters for S3 bucket name.
Enalble binary objects of type '*/*' in settings.
Stage 5 : When user uploads an object, SES send an email to reciever. Receiver uses the API to access the object.

# Versions
Authenticate the API using Cognito Identity/ User pools.
