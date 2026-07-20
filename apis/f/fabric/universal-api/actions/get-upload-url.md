# Fabric: Get Upload URL

Retrieves an upload URL from Fabric.

```
GET https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-upload-url
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fabric `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-upload-url?connectionId=$CONNECTION_ID&filename=Ava%20Chen&size=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filename": "Ava Chen",
  "size": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fabric/latest/actions/get-upload-url?${params}`, {
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
| `filename` | string | yes | Name of the file to upload to Fabric. |
| `size` | number | yes | Size of the file in bytes. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "headers": {
        "contentDisposition": "string"
      },
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `headers` | object |  |
| `headers.contentDisposition` | string |  |
| `url` | string |  |

## Native endpoint

Through the native Fabric API, this operation is `GET /v2/upload` (base URL `https://api.fabric.so`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-upload-url.md) for the provider-specific parameters and requirements.

