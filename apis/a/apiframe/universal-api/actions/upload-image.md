# Apiframe: Upload Image

Uploads an image to Apiframe and returns its URL.

```
POST https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/upload-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Apiframe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/upload-image" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "image": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/apiframe/latest/actions/upload-image', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "image": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `image` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageURL": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageURL` | string |  |

## Native endpoint

Through the native Apiframe API, this operation is `POST /upload` (base URL `https://api.apiframe.pro`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-image.md) for the provider-specific parameters and requirements.

