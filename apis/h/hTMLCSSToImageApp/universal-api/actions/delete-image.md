# HTML/CSS to Image app: Delete Image



```
DELETE https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/delete-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a HTML/CSS to Image app `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/delete-image?connectionId=$CONNECTION_ID&imageId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hTMLCSSToImageApp/latest/actions/delete-image?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `imageId` | string | yes | Identifier of the image to delete. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "imageId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `imageId` | string | Identifier of the deleted image echoed by the wrapper. |

## Native endpoint

Through the native HTML/CSS to Image app API, this operation is `DELETE /v1/image/:imageId` (base URL `https://hcti.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-image.md) for the provider-specific parameters and requirements.

