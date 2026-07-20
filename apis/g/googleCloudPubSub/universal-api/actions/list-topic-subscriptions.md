# Google Cloud Pub/Sub: List Topic Subscriptions

Retrieves subscriptions for a topic in Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-topic-subscriptions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-topic-subscriptions?connectionId=$CONNECTION_ID&limit=25&offset=0&topic=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "topic": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-topic-subscriptions?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `topic` | string | yes | Required. The name of the topic that subscriptions are attached to. Format is `projects/{project}/topics/{topic}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "subscriptions": [
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
| `nextPageToken` | string |  |
| `subscriptions[]` | array<string> |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:topic/subscriptions` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-topic-subscriptions.md) for the provider-specific parameters and requirements.

