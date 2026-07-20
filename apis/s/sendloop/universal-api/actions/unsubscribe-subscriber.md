# Sendloop: Unsubscribe Subscriber



```
PUT https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/unsubscribe-subscriber
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sendloop `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/unsubscribe-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "emailAddress": "ava@example.com",
  "listId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/unsubscribe-subscriber', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "emailAddress": "ava@example.com",
    "listId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `emailAddress` | string | yes | The email address which is going to be unsubscribed |
| `listId` | number | yes | Set the target list ID |
| `unsubscriptionIP` | string | no | Pass 0.0.0.0 if you want to ignore this Default: `0.0.0.0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "redirectURL": "https://example.com",
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `redirectURL` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Sendloop API, this operation is `POST /subscriber.unsubscribe/json` (base URL `https://{{credentials.subdomain}}.sendloop.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/unsubscribe-subscriber.md) for the provider-specific parameters and requirements.

