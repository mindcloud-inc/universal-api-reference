# Rillion Prime Pay: Create Payment Configuration Company



```
POST https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-configuration-company
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Rillion Prime Pay `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-configuration-company" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "companyId": "string",
  "companyName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/rillionPrime/latest/actions/create-payment-configuration-company', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "companyId": "string",
    "companyName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `xCorrelationId` | string | no |  |
| `companyId` | string | yes | Id for the company (from Prime) |
| `companyName` | string | yes | Name for the company (from Prime) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "company": "string",
      "id": "string",
      "name": "Ava Chen",
      "tenantId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `company` | string |  |
| `id` | string |  |
| `name` | string |  |
| `tenantId` | string |  |

## Native endpoint

Through the native Rillion Prime Pay API, this operation is `POST /payment/configuration/company` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-payment-configuration-company.md) for the provider-specific parameters and requirements.

