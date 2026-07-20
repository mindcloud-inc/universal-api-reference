# UniOne: Set Unsubscribed

Adds an email address to UniOne's unsubscribed list.

```
POST https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/set-unsubscribed
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a UniOne `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/set-unsubscribed" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address": "user@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uniOne/latest/actions/set-unsubscribed', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address": "user@example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address` | string | yes | Email address to add to the unsubscribed list. Example: `user@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native UniOne API, this operation is `POST unsubscribed/set.json` (base URL `https://api.unione.io/en/transactional/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/set-unsubscribed.md) for the provider-specific parameters and requirements.

