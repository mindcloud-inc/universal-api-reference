# Microsoft Dynamics 365 BC: Update Costumer SSI



```
PUT https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-costumer-ssi
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Microsoft Dynamics 365 BC `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-costumer-ssi" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "customerId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365BC/latest/actions/update-costumer-ssi', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "customerId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `city` | string | no |  |
| `documentSendingProfile` | string | no |  |
| `no` | string | no |  |
| `address` | string | no |  |
| `postCode` | string | no |  |
| `county` | string | no |  |
| `salespersonCode` | string | no |  |
| `name` | string | no |  |
| `salesforceCustomerNo` | string | no |  |
| `companyId` | string | yes |  |
| `customerId` | string | yes |  |
| `email` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Microsoft Dynamics 365 BC API returns.

## Native endpoint

Through the native Microsoft Dynamics 365 BC API, this operation is `PATCH v2.0/companies(:companyId)/customersSSI(:customerId)` (base URL `https://api.businesscentral.dynamics.com/v2.0/{{credentials.tenantId}}/{{credentials.environment}}/api/ssi/aapi/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-costumer-ssi.md) for the provider-specific parameters and requirements.

