# Rillion Prime Pay: Create Payment Tenant Provider Configuration



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-tenant-provider-configuration
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-tenant-provider-configuration" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "paymentProviderId": 1,
  "configuration": {},
  "configuration.url": "https://example.com",
  "configuration.username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-tenant-provider-configuration', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "paymentProviderId": 1,
    "configuration": {},
    "configuration.url": "https://example.com",
    "configuration.username": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xCorrelationId` | string | no |  |
| `paymentProviderId` | number | yes | Payment provider (0 = Unknown, 1 = Finexio) |
| `configuration` | object | yes | Payment provider configuration |
| `configuration.url` | string | yes | Service URL |
| `configuration.username` | string | yes | Username for Finexio API |
| `configuration.password` | string | no | Password for Finexio API |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Rillion Prime Pay API returns.

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `POST /payment/configuration/tenant/provider` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-tenant-provider-configuration.md) for the provider-specific parameters and requirements.

