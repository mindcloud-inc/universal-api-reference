# Fidel API: Create Missing Transaction Request

Creates a missing transaction request in Fidel API.

```
POST https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-missing-transaction-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fidel API `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-missing-transaction-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "cardId": "string",
  "locationId": "string",
  "amount": 1,
  "transactionDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fidelAPI/latest/actions/create-missing-transaction-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "cardId": "string",
    "locationId": "string",
    "amount": 1,
    "transactionDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cardId` | string | yes |  |
| `locationId` | string | yes | The ID of the location. |
| `amount` | number | yes | Transaction amount in the base currency. |
| `transactionDate` | string | yes | Transaction date in YYYY-MM-DD format. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accountId": "string",
      "amount": 1,
      "brandId": "string",
      "cardId": "string",
      "cardLastNumbers": "string",
      "created": "2026-05-07T12:00:00.000Z",
      "estimatedCompletionDate": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "live": true,
      "locationId": "string",
      "programId": "string",
      "scheme": "string",
      "status": "string",
      "transactionDate": "string",
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accountId` | string |  |
| `amount` | number |  |
| `brandId` | string |  |
| `cardId` | string |  |
| `cardLastNumbers` | string |  |
| `created` | date |  |
| `estimatedCompletionDate` | date |  |
| `id` | string |  |
| `live` | boolean |  |
| `locationId` | string |  |
| `programId` | string |  |
| `scheme` | string |  |
| `status` | string |  |
| `transactionDate` | string |  |
| `updated` | date |  |

## Native endpoint

Through the native Fidel API API, this operation is `POST /cards/:cardId/missing-transaction-requests` (base URL `https://api.fidel.uk/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-missing-transaction-request.md) for the provider-specific parameters and requirements.

