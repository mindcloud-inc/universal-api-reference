# Grok: Update File

Updates a Grok file's metadata or content.

```
PUT https://connect.mindcloud.co/v1/universal/grok/latest/actions/update-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grok `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/grok/latest/actions/update-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/grok/latest/actions/update-file', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileId` | string | yes | File identifier. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Grok API returns.

## Native endpoint

Through the native Grok API, this operation is `PUT /v1/files/:file_id` (base URL `https://api.x.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-file.md) for the provider-specific parameters and requirements.

