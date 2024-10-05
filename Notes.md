
# Notes
Collection of notes to help with running 

## To build
1. Install https://sdkman.io/
1. `sdk install java 17.0.12-tem`
1. `sdk use java 17.0.12-tem`


## To run
1. `cd rest`
1. `../mvnw clean spring-boot:run`

## Send a request
```
$ curl -v localhost:8080/employees
* Host localhost:8080 was resolved.
* IPv6: ::1
* IPv4: 127.0.0.1
*   Trying [::1]:8080...
* Connected to localhost (::1) port 8080
> GET /employees HTTP/1.1
> Host: localhost:8080
> User-Agent: curl/8.7.1
> Accept: */*
> 
* Request completely sent off
< HTTP/1.1 200 
< Content-Type: application/hal+json
< Transfer-Encoding: chunked
< Date: Sat, 05 Oct 2024 13:44:04 GMT
< 
* Connection #0 to host localhost left intact
{"_embedded":{"employeeList":[{"id":1,"name":"Bilbo Baggins","role":"burglar","_links":{"self":{"href":"http://localhost:8080/employees/1"},"employees":{"href":"http://localhost:8080/employees"}}},{"id":2,"name":"Frodo Baggins","role":"thief","_links":{"self":{"href":"http://localhost:8080/employees/2"},"employees":{"href":"http://localhost:8080/employees"}}}]},"_links":{"self":{"href":"http://localhost:8080/employees"}}}%        
```
