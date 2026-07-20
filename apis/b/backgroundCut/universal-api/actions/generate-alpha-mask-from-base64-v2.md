# BackgroundCut: Generate Alpha Mask From Base64 (v2)

Generates an alpha mask in BackgroundCut from a base64 image.

```
POST https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/generate-alpha-mask-from-base64-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BackgroundCut `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/generate-alpha-mask-from-base64-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "imageFileB64": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/backgroundCut/latest/actions/generate-alpha-mask-from-base64-v2', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "imageFileB64": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageFileB64` | string | yes | Base64-encoded source image. |
| `maxResolution` | number | no | Maximum output resolution in pixels, up to 12000000. Example: `4000000`. |
| `returnType` | list | no | Output image format. One of: `0`, `1`, `2`, `3`. Default: `PNG`. |
| `quality` | list | no | Processing quality. One of: `0`, `1`, `2`. Default: `Medium`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        1
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<number> | Binary bytes of the generated alpha mask. |
| `type` | string | Serialized Node buffer type for the returned alpha-mask image. |

## Native endpoint

Through the native BackgroundCut API, this operation is `POST https://api.backgroundcut.co/v2/cut/` (base URL `https://backgroundcut.co/api/v1/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/generate-alpha-mask-from-base64-v2.md) for the provider-specific parameters and requirements.

