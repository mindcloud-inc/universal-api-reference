# Google Cloud Pub/Sub: Delete Schema Revision

Deletes a schema revision from Google Cloud Pub/Sub.

```
DELETE https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-schema-revision
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-schema-revision?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/delete-schema-revision?${params}`, {
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
| `name` | string | yes | Required. The name of the schema revision to be deleted, with a revision ID explicitly included. Example: `projects/123/schemas/my-schema@c7cfa2a8` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "definition": "string",
      "name": "Ava Chen",
      "revisionCreateTime": "string",
      "revisionId": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `definition` | string |  |
| `name` | string |  |
| `revisionCreateTime` | string |  |
| `revisionId` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `DELETE /v1/:name:deleteRevision` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-schema-revision.md) for the provider-specific parameters and requirements.

