# Google Cloud Pub/Sub: Validate Schema

Validates a schema in Google Cloud Pub/Sub.

```
GET https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/validate-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Google Cloud Pub/Sub `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/validate-schema?connectionId=$CONNECTION_ID&parent=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "parent": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleCloudPubSub/latest/actions/validate-schema?${params}`, {
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
| `parent` | string | yes | Required. The name of the project in which to validate schemas. Format is `projects/{project-id}`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Google Cloud Pub/Sub API returns.

## Native endpoint

Through the native Google Cloud Pub/Sub API, this operation is `POST /v1/:parent/schemas:validate` (base URL `https://pubsub.googleapis.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/validate-schema.md) for the provider-specific parameters and requirements.

