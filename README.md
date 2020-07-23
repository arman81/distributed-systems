# distributed-systems
Communication between different components in distributed systems:

Communication between Different components in a distributed system can happen via different ways.
One of the most common ways is Via HTTP Calls:

HTTP Call format :

Method Type /post |  Uri path /path for request handler | HTTP versio e.g. HTTP 1.1 - this will serve as basis for communication
HTTP Version | status code : 1xx, 2xx, 3xx, 4xx, 5xx | response message ->> this header is for response message

Header: Key value pairs denoting the message type
e.g. Content-length : 34
     content-type : json etc.
     content-encoding : gzip : shows algo to use to decompress data
custom headers can also be added like X-test , for AB testing etc.

Message Body


HTTP 1.1 : first creates a HTTP connection and then send the request over that connection, if the connection is blocking a new connection is created for subsequent request
	   headers data is plain text 

HTTP 2 : sends multiple requests by breaking into streams over the same connection
	headers are compressed so is efficient but it is hard to debug


1. Get Http call :
	for e.g. : A service in distributed system which checks the health of all the servers in the network can make a GET call to each server to check for health.

2. POST Call:
	Non idempotent, can have effects on server, expected to perform computation 
