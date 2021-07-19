Getting rest api up and running

go mod init myweb/simplemux
go get github.com/gorilla/mux@latest

curl http://localhost:5000/api/v1/
Welcome to the REST API!


Registering additional paths

params := mux.Vars(r)

curl http://localhost:5000/api/v1/courses

List of all courses.

curl http://localhost:5000/api/v1/courses/123

Detail for course 123

Passing in query string

curl "http://localhost:5000/api/v1/courses? country=JP&state=Osaka"

Specifying request methods

Option Purpose Example
-X To specify an HTTP request method POST
-H To specify request headers "Content-type: application/json"
-d To specify request data '{"message":"HelloData"}' --data-binary To specify binary request data @file.bin
-i To show the response headers
-u To specify username and password "admin:secret"
-v To enable verbose mode, which outputs information such as request and response headers and errors