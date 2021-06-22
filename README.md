Web Database Tool
=================

Create an in-memory key/value database with http interface to store arbitrary chunks of data.

Keys are non-empty strings consisting of 26 lowercase latin letters, numbers, dash `-`, or underscore `_`, starting with letter or underscore character. Keys should be no longer than 16 characters.

Values are arbitrary non-empty byte arrays up to 500 bytes in size. 

### Requirements

* The application should provide http endpoints:
  * `POST /set/{key}` -- Sets key/value entry to `key` and contents of the request body.
  * `GET /retrieve/{key}` -- Returns value associated with `key`. 
  * `GET /exists/{key}` -- Returns `true` or `false` as response indicating whether `key` contains any value.
  * `DELETE /remove/{key}` -- Should remove the key/value pair from the storage if it is present.
* Every endpoint should return appropriate HTTP status code.
* Maximum number of stored keys is limited to 1000.
* All input data should be validated against requirements with appropriate responses.
* Use standard go library only.
* Push your code into GitHub repository, setting up appropriate GitHub actions.
* Use approaches and practices as you would do with any real production ready code.
