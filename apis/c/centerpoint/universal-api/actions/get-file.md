# Centerpoint: Get File



```
GET https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-file
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Centerpoint `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-file?connectionId=$CONNECTION_ID&FILE_ID=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "FILE_ID": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/centerpoint/latest/actions/get-file?${params}`, {
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
| `FILE_ID` | number | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {
        "createdAt": "string",
        "deletedAt": {},
        "height": {},
        "latitude": 1,
        "longitude": 1,
        "mimeType": "string",
        "thumbnailUrl": "https://example.com",
        "title": {},
        "updatedAt": "string",
        "url": "https://example.com",
        "variety": "string",
        "width": {}
      },
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes.createdAt` | string |  |
| `attributes.deletedAt` | object |  |
| `attributes.height` | object |  |
| `attributes.latitude` | number |  |
| `attributes.longitude` | number |  |
| `attributes.mimeType` | string |  |
| `attributes.thumbnailUrl` | string |  |
| `attributes.title` | object |  |
| `attributes.updatedAt` | string |  |
| `attributes.url` | string |  |
| `attributes.variety` | string |  |
| `attributes.width` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Centerpoint API, this operation is `GET files/:FILE_ID` (base URL `https://api.centerpointconnect.io/centerpoint/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-file.md) for the provider-specific parameters and requirements.

