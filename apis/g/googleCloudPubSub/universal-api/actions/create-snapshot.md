# Google Cloud Pub/Sub: Create Snapshot

Creates a snapshot in Google Cloud Pub/Sub.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/create-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/create-snapshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/create-snapshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Required. User-provided name for this snapshot. Format is `projects/{project}/snapshots/{snap}`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "expireTime": "string",
      "name": "Ava Chen",
      "topic": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `expireTime` | string |  |
| `name` | string |  |
| `topic` | string |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `PUT /v1/:name` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-snapshot.md) for the provider-specific parameters and requirements.

