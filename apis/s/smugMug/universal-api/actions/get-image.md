# SmugMug: Get Image



```
GET https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/get-image
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmugMug `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/get-image?connectionId=$CONNECTION_ID&imageUriId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageUriId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smugMug/latest/actions/get-image?${params}`, {
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
| `imageUriId` | string | yes | SmugMug image identifier including any URI suffix. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Code": 1,
      "Message": "string",
      "Options": {},
      "Response": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Code` | number | Provider status code returned by SmugMug. |
| `Message` | string | Provider status message returned by SmugMug. |
| `Options` | object | Provider-declared request options and parameter metadata when returned by SmugMug. |
| `Response` | object | Raw SmugMug response payload for the requested resource or collection. |

## Native endpoint

Through the native SmugMug API, this operation is `GET /image/:imageUriId` (base URL `https://api.smugmug.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image.md) for the provider-specific parameters and requirements.

