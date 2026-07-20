# Google Cloud Pub/Sub: List Schemas

Retrieves schemas from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-schemas?connectionId=$CONNECTION_ID&limit=25&offset=0&parent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "parent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/list-schemas?${params}`, {
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
| `parent` | string | yes | Required. The name of the project in which to list schemas. Format is `projects/{project-id}`. |
| `view` | string | no | The set of Schema fields to return in the response. If not set, returns Schemas with `name` and `type`, but not `definition`. Set to `FULL` to retrieve all fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageToken": "string",
      "schemas": [
        {
          "definition": "string",
          "name": "Ava Chen",
          "revisionCreateTime": "string",
          "revisionId": "string",
          "type": "string"
        }
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
| `schemas[].definition` | string |  |
| `schemas[].name` | string |  |
| `schemas[].revisionCreateTime` | string |  |
| `schemas[].revisionId` | string |  |
| `schemas[].type` | string |  |

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:parent/schemas` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-schemas.md) for the provider-specific parameters and requirements.

