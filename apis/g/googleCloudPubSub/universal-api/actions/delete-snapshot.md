# Google Cloud Pub/Sub: Delete Snapshot

Deletes a snapshot from Google Cloud Pub/Sub.

```
DELETE https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-snapshot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-snapshot?connectionId=$CONNECTION_ID&snapshot=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "snapshot": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-snapshot?${params}`, {
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
| `snapshot` | string | yes | Required. The name of the snapshot to delete. Format is `projects/{project}/snapshots/{snap}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Pub/Sub API returns.

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `DELETE /v1/:snapshot` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-snapshot.md) for the provider-specific parameters and requirements.

