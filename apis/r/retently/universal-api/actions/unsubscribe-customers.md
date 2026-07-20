# Retently: Unsubscribe Customers

Unsubscribes customers from surveys in Retently.

```
PUT https://connect.mindcloud.co/v1/universal/retently/latest/actions/unsubscribe-customers
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Retently `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/retently/latest/actions/unsubscribe-customers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "subscribers[]": [
    "string"
  ],
  "subscribers[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/retently/latest/actions/unsubscribe-customers', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "subscribers[]": ["string"],
    "subscribers[].email": "ava@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `message` | string | no | Opt out message |
| `subscribers[]` | array<string> | yes | An array of subscriber emails |
| `subscribers[].email` | string | yes | Email address |

## Response

```json
{
  "success": true,
  "data": [
    {
      "email": "ava@example.com",
      "unsubscribed": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string |  |
| `unsubscribed` | boolean |  |

## Native endpoint

Through the native Retently API, this operation is `POST /api/v2/customers/unsubscribe` (base URL `https://app.retently.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-customers.md) for the provider-specific parameters and requirements.

