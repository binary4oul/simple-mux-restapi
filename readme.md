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

