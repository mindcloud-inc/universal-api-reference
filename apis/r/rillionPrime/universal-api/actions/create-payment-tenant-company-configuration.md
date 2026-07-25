# Rillion Prime Pay: Create Payment Tenant Company Configuration



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-tenant-company-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-tenant-company-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "configurations[].configuration": {},
  "paymentProviderId": 1,
  "configurations[]": [
    {}
  ],
  "configurations[].configuration.companyId": "string",
  "configurations[].configuration.buyerId": "string",
  "configurations[].configuration.buyerName": "Ava Chen",
  "configurations[].configuration.bankAccountIdentifier": 1,
  "configurations[].configuration.startDate": "2026-05-07T12:00:00.000Z"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-tenant-company-configuration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "configurations[].configuration": {},
    "paymentProviderId": 1,
    "configurations[]": [{}],
    "configurations[].configuration.companyId": "string",
    "configurations[].configuration.buyerId": "string",
    "configurations[].configuration.buyerName": "Ava Chen",
    "configurations[].configuration.bankAccountIdentifier": 1,
    "configurations[].configuration.startDate": "2026-05-07T12:00:00.000Z"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `configurations[].configuration` | object | yes | Company configuration |
| `xCorrelationId` | string | no |  |
| `paymentProviderId` | number | yes | Payment provider (0 = Unknown, 1 = Finexio) |
| `configurations[]` | array<object> | yes |  |
| `configurations[].configuration.companyId` | string | yes | Company Id |
| `configurations[].configuration.buyerId` | string | yes | Buyer identification |
| `configurations[].configuration.buyerName` | string | yes | Name of the buyer |
| `configurations[].configuration.bankAccountIdentifier` | number | yes | Last four digits of bank account identifier |
| `configurations[].configuration.startDate` | date | yes | Date for where payment processing should start |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Pay API returns.

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `POST /payment/configuration/tenant/company` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-tenant-company-configuration.md) for the provider-specific parameters and requirements.

