# MoneyBird: Send Estimate

Sends an existing estimate from MoneyBird.

```
PUT https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/send-estimate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MoneyBird `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/send-estimate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "administrationId": "string",
  "estimateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moneyBird/latest/actions/send-estimate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "administrationId": "string",
    "estimateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `administrationId` | string | yes | Moneybird administration ID. |
| `estimateId` | string | yes | Moneybird estimate ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "acceptedAt": "2026-05-07T12:00:00.000Z",
      "administrationId": "string",
      "contact": {},
      "contactId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "currency": "string",
      "details": [
        {}
      ],
      "dueDate": "2026-05-07T12:00:00.000Z",
      "estimateDate": "2026-05-07T12:00:00.000Z",
      "estimateId": "string",
      "id": "string",
      "reference": "string",
      "rejectedAt": "2026-05-07T12:00:00.000Z",
      "sentAt": "2026-05-07T12:00:00.000Z",
      "state": "string",
      "totalPriceExclTax": "string",
      "totalPriceInclTax": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `acceptedAt` | date |  |
| `administrationId` | string |  |
| `contact` | object |  |
| `contactId` | string |  |
| `createdAt` | date |  |
| `currency` | string |  |
| `details` | array<object> |  |
| `dueDate` | date |  |
| `estimateDate` | date |  |
| `estimateId` | string |  |
| `id` | string |  |
| `reference` | string |  |
| `rejectedAt` | date |  |
| `sentAt` | date |  |
| `state` | string |  |
| `totalPriceExclTax` | string |  |
| `totalPriceInclTax` | string |  |
| `updatedAt` | date |  |
| `version` | number |  |

## Native endpoint

Through the native MoneyBird API, this operation is `PATCH /:administrationId/estimates/:estimateId/send_estimate.json` (base URL `https://moneybird.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-estimate.md) for the provider-specific parameters and requirements.

