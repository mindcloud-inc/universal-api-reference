# Voog: Create Asset

Creates a new asset in the current Voog site.

```
POST https://connect.mindcloud.co/v1/universal/voog/latest/actions/create-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Voog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/voog/latest/actions/create-asset" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "filename": "Ava Chen",
  "size": 1,
  "contentType": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/voog/latest/actions/create-asset', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "filename": "Ava Chen",
    "size": 1,
    "contentType": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `filename` | string | yes | Filename for the asset to create. |
| `size` | number | yes | File size in bytes. |
| `contentType` | string | yes | MIME type of the asset file. |
| `width` | number | no | Image width in pixels when available. |
| `height` | number | no | Image height in pixels when available. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Voog API returns.

## Native endpoint

Through the native Voog API, this operation is `POST /assets` (base URL `{{credentials.siteUrl}}/admin/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-asset.md) for the provider-specific parameters and requirements.

