# QStash: Publish Message

Publishes a message to a QStash destination.

```
POST https://connect.mindcloud.co/v1/universal/qStash/latest/actions/publish-message
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a QStash `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/qStash/latest/actions/publish-message" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "destination": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/qStash/latest/actions/publish-message', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "destination": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `destination` | string | yes | Destination URL or URL Group name. |
| `body` | string | no | Raw request message to deliver. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "deduplicated": true,
      "messageId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `deduplicated` | boolean |  |
| `messageId` | string |  |
| `url` | string |  |

## Native endpoint

Through the native QStash API, this operation is `POST /v2/publish/:destination` (base URL `https://qstash-eu-central-1.upstash.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-message.md) for the provider-specific parameters and requirements.

