# MOBIDI: Generate Image Thumbnail

Generates an image thumbnail for a MOBIDI attachment.

```
PUT https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/generate-image-thumbnail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MOBIDI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/generate-image-thumbnail" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "recordId": "string",
  "attachmentId": "string",
  "maxSize": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mOBIDI/latest/actions/generate-image-thumbnail', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "recordId": "string",
    "attachmentId": "string",
    "maxSize": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `recordId` | string | yes | MOBIDI record identifier. |
| `attachmentId` | string | yes | Attachment identifier. |
| `maxSize` | number | yes | Maximum thumbnail size in pixels. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MOBIDI API returns.

## Native endpoint

Through the native MOBIDI API, this operation is `POST /MobidiQueryManagerHandler` (base URL `https://servis2.dece.com.tr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-image-thumbnail.md) for the provider-specific parameters and requirements.

