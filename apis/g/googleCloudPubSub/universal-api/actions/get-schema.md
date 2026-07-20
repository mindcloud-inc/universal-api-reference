# Google Cloud Pub/Sub: Get Schema

Retrieves a schema from Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-schema?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/get-schema?${params}`, {
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
| `name` | string | yes | Required. The name of the schema to get. Format is `projects/{project}/schemas/{schema}`. |
| `view` | string | no | The set of fields to return in the response. If not set, returns a Schema with all fields filled out. Set to `BASIC` to omit the `definition`. |

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

Through the native Google Cloud Pub/Sub API, this operation is `GET /v1/:name` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schema.md) for the provider-specific parameters and requirements.

