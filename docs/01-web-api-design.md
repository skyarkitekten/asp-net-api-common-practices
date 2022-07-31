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

## HTTP Status Codes

## Resources and Routes

## ASP.NET Response Types

## Versioning


### Links
1. [RESTful web API design](https://docs.microsoft.com/en-us/azure/architecture/best-practices/api-design)
