# Google Cloud Pub/Sub: Get Snapshot

Retrieves a snapshot from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-snapshot?connectionId=$CONNECTION_ID&snapshot=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "snapshot": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-snapshot?${params}`, {
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
| `snapshot` | string | yes | Required. The name of the snapshot to get. Format is `projects/{project}/snapshots/{snap}`. |

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

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:snapshot` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-snapshot.md) for the provider-specific parameters and requirements.

