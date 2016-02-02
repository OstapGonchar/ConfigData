# "Microservices with Spring" Udemy course configuration

### Worflow (what's happening)
1. Spring Cloud Clients access local Spring Cloud Config server for locating configuration
2. Spring Cloud Config server provides with configuration loaded from this GIT repository
3. Since Eureka is present in dependencies and config - clients are registered in Eureka Service Discovery
4. Clients use Ribbon Client Load Balancer for balanced requests
5. Clients use Feign for simplyfing REST calls to other Microservices (Clients)
6. Hystrix (Circuit Breaker) is configured on Client for fallback behaviour

Another way is to use Zuul API Gateway (includes both Hystrix and Ribbon)
