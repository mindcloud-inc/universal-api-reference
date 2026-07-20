# Pastefy: Update Paste



```
PUT https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/update-paste
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pastefy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/update-paste" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pastefy/latest/actions/update-paste', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `content` | string | no |  |
| `encrypted` | boolean | no |  |
| `expireAt` | string | no |  |
| `folder` | string | no |  |
| `id` | string | yes |  |
| `tags[]` | array<string> | no |  |
| `title` | string | no |  |
| `type` | string | no |  |
| `visibility` | string | no |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pastefy API returns.

## Native endpoint

Through the native Pastefy API, this operation is `PUT /paste/:id` (base URL `https://pastefy.app/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-paste.md) for the provider-specific parameters and requirements.

