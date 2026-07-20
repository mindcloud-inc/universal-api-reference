# Flotiq: Batch Publish Content Objects

Publishes multiple content objects in Flotiq.

```
PUT https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-publish-content-objects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flotiq `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-publish-content-objects" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "body": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flotiq/latest/actions/batch-publish-content-objects', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "body": {}
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | The content type name that owns the objects. |
| `body` | object | yes | The batch publish payload. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Flotiq API returns.

## Native endpoint

Through the native Flotiq API, this operation is `POST /content/{{name}}/batch-publish` (base URL `https://api.flotiq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/batch-publish-content-objects.md) for the provider-specific parameters and requirements.

