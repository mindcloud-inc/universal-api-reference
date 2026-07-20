# Housecall Pro: Create Lead



```
POST https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Housecall Pro `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/housecallPro/latest/actions/create-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customerId` | string | no | Either this or Customer is required. |
| `leadSource` | string | no |  |
| `note` | string | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `customer` | object | no | Either this or Customer ID is required. |
| `addressId` | string | no |  |
| `address` | object | no |  |
| `assignedEmployeeId` | string | no |  |
| `tags[]` | array<string> | no |  |
| `lineItems[]` | array<object> | no |  |
| `taxName` | string | no |  |
| `taxRate` | number | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "assignedEmployee": {},
      "companyId": "string",
      "companyName": "Ava Chen",
      "conversions": [
        {}
      ],
      "customer": {},
      "id": "string",
      "leadSource": "string",
      "lostAt": "2026-05-07T12:00:00.000Z",
      "number": 1,
      "pipelineStatus": "string",
      "status": "string",
      "tags": [
        "string"
      ],
      "totalAmount": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object | Lead address details. |
| `assignedEmployee` | object | Assigned employee. |
| `companyId` | string | Company ID. |
| `companyName` | string | Company name. |
| `conversions` | array<object> | Lead conversions. |
| `customer` | object | Customer attached to the lead. |
| `id` | string | Lead ID. |
| `leadSource` | string | Lead source. |
| `lostAt` | date | Timestamp when the lead was marked lost. |
| `number` | number | Lead number. |
| `pipelineStatus` | string | Pipeline status. |
| `status` | string | Lead status. |
| `tags` | array<string> | Lead tags. |
| `totalAmount` | number | Lead total amount. |

## Native endpoint

Through the native Housecall Pro API, this operation is `POST /leads` (base URL `https://api.housecallpro.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-lead.md) for the provider-specific parameters and requirements.

