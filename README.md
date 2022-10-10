# ApiGateway-proxy


Sequence to start services:
---------------------------
1. Start KeyCloak server
2. Start DiscoveryService
3. Start ApiGateway
4. Start ResourceServer
5. Start albums
6. Start photos
7. Start spa-example
8. Start PhotoAppWebClient 

There are three API gateway implementations :
---------------------------
1. spring-cloud-gateway-as-ouath2-client - Implementation of Spring Cloud API Gateway and its acting as oauth client for authorization_code flow
2. api-gateway-as-both-resourceserver-and-oauth-client-redis-session - Implementation of Spring Cloud API Gateway which also acts as a OAuth client and Resource server. Supports both authrorization_code flow for UI flow and token in Authorization header for API calls from 3rd party.
3. ApiGateway - Implementation of Spring Cloud API Gateway and just doing routing 

Few test URLS:
----------------
 - http://localhost:8082/albums
 - http://localhost:8082users/status/check
 - http://localhost:8082/users/status/check/unprotected
 - http://localhost:8181/index.html
 - try photoappwebclient's API
