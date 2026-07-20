# Refrens: Create Expenditure



```
POST https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-expenditure
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Refrens `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-expenditure" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "billedBy": {},
  "items[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/refrens/latest/actions/create-expenditure', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "billedBy": {},
    "items[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `billedBy` | object | yes |  |
| `items[]` | array<object> | yes |  |
| `invoiceDate` | date | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_id": "string",
      "billedBy": {},
      "billedTo": {},
      "billType": "string",
      "client": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "finalTotal": {},
      "invoiceDate": "2026-05-07T12:00:00.000Z",
      "invoiceNumber": "string",
      "items": [
        {}
      ],
      "share": {},
      "status": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string |  |
| `billedBy` | object |  |
| `billedTo` | object |  |
| `billType` | string |  |
| `client` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `finalTotal` | object |  |
| `invoiceDate` | date |  |
| `invoiceNumber` | string |  |
| `items` | array<object> |  |
| `share` | object |  |
| `status` | string |  |
| `updatedAt` | date |  |

## Native endpoint

Through the native Refrens API, this operation is `POST /businesses/:urlKey/expenditures` (base URL `https://api.refrens.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-expenditure.md) for the provider-specific parameters and requirements.

