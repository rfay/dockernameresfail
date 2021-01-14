This is a trivial example of a docker-compose name resolution.

The assumption is that a second docker-compose recipe should not have name resolution for another one.

`docker-compose -f main.yaml up` brings up the first docker-compose project, which has a service named "first"

`docker-compose -f second.yaml up` brings up a second docker-compose project and tries to ping the service "first" by name. It should not be able to even look it up. Why is it able to ping "first"?
