# Visma eAccounting: Update Quote

Updates an existing quote in Visma eAccounting.

```
PUT https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/update-quote
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Visma eAccounting `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/update-quote" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vismaEAccounting/latest/actions/update-quote', {
  method: 'PUT',
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



## Response

```json
{
  "success": true,
  "data": [
    {
      "currencyCode": "string",
      "customerId": "string",
      "customerName": "Ava Chen",
      "customerNumber": "string",
      "dueDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "quoteDate": "2026-05-07T12:00:00.000Z",
      "rows": [
        [
          {}
        ]
      ],
      "status": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currencyCode` | string |  |
| `customerId` | string |  |
| `customerName` | string |  |
| `customerNumber` | string |  |
| `dueDate` | date |  |
| `id` | string |  |
| `quoteDate` | date |  |
| `rows[]` | array<object> |  |
| `rows[].id` | string |  |
| `rows[].quantity` | number |  |
| `rows[].text` | string |  |
| `rows[].unitPrice` | number |  |
| `status` | number |  |

## Native endpoint

Through the native Visma eAccounting API, this operation is `PUT /quotes/{id}` (base URL `https://eaccountingapi.vismaonline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-quote.md) for the provider-specific parameters and requirements.

