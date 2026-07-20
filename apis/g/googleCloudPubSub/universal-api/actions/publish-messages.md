# Google Cloud Pub/Sub: Publish Messages

Publishes messages to a topic in Google Cloud Pub/Sub.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/publish-messages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/publish-messages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "topic": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/publish-messages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "topic": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topic` | string | yes | Required. The messages in the request will be published on this topic. Format is `projects/{project}/topics/{topic}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "messageIds": [
        [
          "string"
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `messageIds[]` | array<string> |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `POST /v1/:topic:publish` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/publish-messages.md) for the provider-specific parameters and requirements.

