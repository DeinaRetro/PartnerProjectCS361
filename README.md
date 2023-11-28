# Macro-Counter
A minimal macro counter React app with REST API backend connected to a MongoDB collection.

# Poe-Poems Microservice
A microservice that can retrieve (all entries or filtered entries), update/edit, and delete data on a MongoDB collection

---------------------------------------------------------------------------------------------------------------------------------------------------------------------
# Example Requests:
POST http://localhost:5000/poems HTTP/1.1
content-type: application/json

{
    "name": "Silence",
    "poem": "    "
}


PUT http://localhost:5000/poems/65657e0e2807cb82fcf17429/ HTTP/1.1
content-type: application/json

{
    "name": "Cookie",
    "poem": "Delicious, but also not a poem. <br>This is another test input."
}


GET http://localhost:5000/poems HTTP/1.1


DELETE http://localhost:5000/poems/65657e922807cb82fcf17437/ HTTP/1.1

---------------------------------------------------------------------------------------------------------------------------------------------------------------------

Data is returned as an HTML Response.
Any changes made return an HTML Response body (other than DELETE, which only sends back a 204 status code for successful deletions).
A 200 status code means changes were successful, a 404 is not found, and a 400 is a bad request.

UML Sequence Diagram:
![CS361Microservice](https://github.com/DeinaRetro/PartnerProjectCS361/assets/86344289/12b67896-c8af-4084-ba45-9b2054317bd1)


