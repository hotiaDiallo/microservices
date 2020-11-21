# Currency Conversion Micro Service
Run com.ibra.microservices.currencyconversionservice.CurrencyConversionServiceApplication as a Java Application.

## Resources

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

## Containerization

### Creating Containers

- mvn package

### Running Containers

```
docker run --publish 8100:8100 --network currency-network --env CURRENCY_EXCHANGE_URI=http://currency-exchange-service:8000 ibra/currency-conversion-service:0.0.1-SNAPSHOT
```

#### Test API 
- http://localhost:8100/currency-converter/from/EUR/to/INR/quantity/10
