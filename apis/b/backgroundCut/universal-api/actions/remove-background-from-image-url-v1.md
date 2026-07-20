# BackgroundCut: Remove Background From Image URL (v1)

Removes an image background in BackgroundCut from an image URL.

```
POST https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/remove-background-from-image-url-v1
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BackgroundCut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/remove-background-from-image-url-v1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/remove-background-from-image-url-v1', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileUrl": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `fileUrl` | string | yes | Public URL of the source image. |
| `maxResolution` | number | no | Maximum output resolution in pixels, up to 12000000. Example: `4000000`. |
| `returnFormat` | list | no | Output format. One of: `0`, `1`. Default: `PNG`. |
| `quality` | list | no | Processing quality. One of: `0`, `1`, `2`. Default: `Medium`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "outputImageUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `outputImageUrl` | string | Public URL of the generated background-removed image. |

## Native endpoint

Through the native BackgroundCut API, this operation is `POST cut/` (base URL `https://backgroundcut.co/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/remove-background-from-image-url-v1.md) for the provider-specific parameters and requirements.

