# Google Cloud Pub/Sub: Create Schema

Creates a schema in Google Cloud Pub/Sub.

```
POST https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/create-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/create-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "parent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/create-schema', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "parent": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `parent` | string | yes | Required. The name of the project in which to create the schema. Format is `projects/{project-id}`. |
| `schemaId` | string | no | The ID to use for the schema, which will become the final component of the schema's resource name. See https://cloud.google.com/pubsub/docs/pubsub-basics#resource_names for resource name constraints. |

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

Through the native Google Cloud Pub/Sub API, this operation is `POST /v1/:parent/schemas` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-schema.md) for the provider-specific parameters and requirements.

