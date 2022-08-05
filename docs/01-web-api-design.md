# Web API Design

Most API's are built on Representational State Transfer (REST) principles. REST is defined as

>  an architectural style for building distributed systems based on hypermedia...designed around resources.

Hypermedia is...

Resources are...have identifier that is a URI. 

These are generally accpeted conventions and will frustrate consumers of your API if you do follow them.
- use nouns not verbs:

- DO: `/customers`
- DO NOT: `/getCustomers`

Use plural, not singular:

Append the identifier for a specific resource

- DO: `customers/2939`

The general template for creating RESTful URI's should be:

`/{collection}/{identifier}`
`/{collection}/{identifier}/{childCollection}/{childIdentifier`

## REST vs RPC

REST is about state, not behavior

How to model REST when commands:

    - TODO

## HTTP Verbs

You should design your API to support the verbs defined in the HTTP Spec.

| HTTP VERB | Purpose | Idempotent | Safe | 
| --------- | :------------------- | :---:| :---: | 
| GET | request a resource | yes | yes
| POST | add a resource | no | no 
| PUT | update a resource's state | yes | no
| DELETE | delete a resource | yes | no
| PATCH | updates part of a resource | yes | no
| HEAD | request a resource but only return header data | yes | yes
| OPTIONS | request info on how to work with a resource 

**Idempotence**: idempotent methods that produce the same effect when called once or more than once.

**Safety**: does not change the system's state

The most common verbs are GET, PUT, POST, and DELETE. Be careful when using less common verbs.


## HTTP Status Codes

- 100-199: Informational
- 200-299: Successful
- 300-399: Redirection
- 400-499: Client Error
- 500-599: Server Error

According to the HTTP Spec, a client **must** understand the class of status code indicated be the first digit.

## Resources and Routes

## ASP.NET Response Types

## Versioning


### Links
1. [RESTful web API design](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
