# Dubble: Create Webhook for Collection

Creates a new webhook for a collection in Dubble.

```
POST https://connect.mindcloud.co/v1/universal/dubble/latest/actions/create-webhook-for-collection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dubble `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dubble/latest/actions/create-webhook-for-collection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "collectionId": "string",
  "targetUrl": "https://example.com",
  "triggers[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dubble/latest/actions/create-webhook-for-collection', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "collectionId": "string",
    "targetUrl": "https://example.com",
    "triggers[]": ["string"]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `collectionId` | string | yes | The ID of the collection |
| `name` | string | no | Optional name for the webhook |
| `targetUrl` | string | yes | The URL where the webhook will send data |
| `triggers[]` | array<string> | yes | Trigger events for the webhook |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Dubble API returns.

## Native endpoint

Through the native Dubble API, this operation is `POST /webhooks/:collectionId` (base URL `https://api.dubble.so/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-webhook-for-collection.md) for the provider-specific parameters and requirements.

