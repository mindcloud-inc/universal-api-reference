# Facebook: Create Page Photo



```
POST https://connect.mindcloud.co/v1/universal/facebook/latest/actions/create-page-photo
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Facebook `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/facebook/latest/actions/create-page-photo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "pageId": "string",
  "url": "https://example.com/photo.jpg"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/facebook/latest/actions/create-page-photo', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "pageId": "string",
    "url": "https://example.com/photo.jpg"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `pageId` | list<string> | yes |  |
| `url` | string | yes | Public image URL. JPEG, BMP, PNG, GIF, or TIFF up to 10 MB. Example: `https://example.com/photo.jpg`. |
| `caption` | string | no |  |
| `published` | boolean | no | Set to false to upload without publishing. Unpublished photos are deleted after about 24 hours unless published. Default: `true`. |
| `scheduledPublishTime` | date | no | Set Published to false when scheduling. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Facebook API returns.

## Native endpoint

Through the native Facebook API, this operation is `POST /:pageId/photos` (base URL `https://graph.facebook.com/v25.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-page-photo.md) for the provider-specific parameters and requirements.

