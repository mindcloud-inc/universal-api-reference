# nandbox: Download Media File

Retrieves a media file from nandbox by media ID.

```
GET https://connect.mindcloud.co/v1/universal/nandbox/latest/actions/download-media-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a nandbox `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nandbox/latest/actions/download-media-file?connectionId=$CONNECTION_ID&mediaId=123456789.jpg" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "mediaId": "123456789.jpg"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nandbox/latest/actions/download-media-file?${params}`, {
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
| `mediaId` | string | yes | Unique media identifier returned by nandbox for a previously uploaded file. Example: `123456789.jpg`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response` | object | Raw binary response body returned by the nandbox download endpoint. |

## Native endpoint

Through the native nandbox API, this operation is `GET {{mediaId}}` (base URL `{{credentials.downloadServer}}/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-media-file.md) for the provider-specific parameters and requirements.

