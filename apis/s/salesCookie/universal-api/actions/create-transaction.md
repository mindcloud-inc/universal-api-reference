# Sales Cookie: Create Transaction

Creates or updates a transaction in Sales Cookie by unique ID.

```
POST https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sales Cookie `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "date": "2026-05-07T12:00:00.000Z",
  "uniqueId": "string",
  "revenue": 1,
  "currency": "string",
  "owner1": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/salesCookie/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "date": "2026-05-07T12:00:00.000Z",
    "uniqueId": "string",
    "revenue": 1,
    "currency": "string",
    "owner1": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `date` | date | yes | Transaction date in ISO 8601 format. |
| `uniqueId` | string | yes | Unique transaction identifier. |
| `revenue` | number | yes |  |
| `currency` | string | yes |  |
| `transactionStatus` | string | no |  |
| `owner1` | string | yes | Primary credited user alias or name. |
| `customer` | string | no |  |
| `product` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "currency": "string",
      "customer": "string",
      "date": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "owner1": "string",
      "product": "string",
      "revenue": 1,
      "transactionStatus": "string",
      "uniqueId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `currency` | string |  |
| `customer` | string |  |
| `date` | date |  |
| `id` | string |  |
| `owner1` | string |  |
| `product` | string |  |
| `revenue` | number |  |
| `transactionStatus` | string |  |
| `uniqueId` | string |  |

## Native endpoint

Through the native Sales Cookie API, this operation is `POST /Api/CreateTransaction` (base URL `https://salescookie.com/app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.

