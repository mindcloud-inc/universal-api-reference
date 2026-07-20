# Docage: Create Transaction

Creates a new transaction in Docage.

```
POST https://connect.mindcloud.co/v1/universal/docage/latest/actions/create-transaction
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docage `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docage/latest/actions/create-transaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "isTest": true,
  "name": "Ava Chen",
  "reminder": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docage/latest/actions/create-transaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "isTest": true,
    "name": "Ava Chen",
    "reminder": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `isTest` | boolean | yes | Whether to create the transaction as a test. |
| `name` | string | yes | The transaction name. |
| `reminder` | number | yes | Reminder cadence enum value: 0, 1, 2, 7, 14, or 30. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | string |  |

## Native endpoint

Through the native Docage API, this operation is `POST /Transactions` (base URL `https://api.docage.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-transaction.md) for the provider-specific parameters and requirements.

