# Tellephant: Update unsubscribe status

Updates contact subscription status in Tellephant.

```
PUT https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-unsubscribe-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Tellephant `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-unsubscribe-status" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    "string"
  ],
  "type": "block"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tellephant/latest/actions/update-unsubscribe-status', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": ["string"],
    "type": "block"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contacts[]` | array<string> | yes | Array of contact phone numbers. |
| `type` | list | yes | Unsubscribe operation type: unsubscribe, subscribe, block, or unblock. One of: `block`, `subscribe`, `unblock`, `unsubscribe`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "error": {},
      "message": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `error` | object |  |
| `message` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Tellephant API, this operation is `POST /v1/user/unsubscribe/update` (base URL `https://api.tellephant.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-unsubscribe-status.md) for the provider-specific parameters and requirements.

