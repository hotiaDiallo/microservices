# microservices

## Containerization

### Creating images

- cd currency-conversion-service/
- mvn package
- created image : ibra/currency-conversion-service:0.0.1-SNAPSHOT

- cd currency-exchange-service/
- mvn package
- created image : ibra/currency-exchange-service:0.0.1-SNAPSHOT

- cd netflix-eureka-naming-server/
- mvn package
- created image : ibra/netflix-eureka-naming-server:0.0.1-SNAPSHOT

- cd netflix-zuul-api-gateway-server/
- mvn package
- created image : ibra/netflix-zuul-api-gateway-server:0.0.1-SNAPSHOT

### Running Containers

- docker-compose up

#### Test API 
- http://localhost:8100/currency-converter/from/EUR/to/INR/quantity/10

```json
{
id: 10002,
from: "EUR",
to: "INR",
conversionMultiple: 75,
quantity: 10,
totalCalculatedAmount: 750
}
```

- http://localhost:8100/currency-converter/from/EUR/to/INR/quantity/10
```json
{
id: 10002,
from: "EUR",
to: "INR",
conversionMultiple: 75,
quantity: 10,
totalCalculatedAmount: 750
}
```
