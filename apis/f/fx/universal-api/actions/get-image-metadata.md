# 1001fx: Get Image Metadata

Retrieves metadata from an image file.

```
GET https://connect.mindcloud.co/v1/universal/fx/latest/actions/get-image-metadata
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a 1001fx `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fx/latest/actions/get-image-metadata?connectionId=$CONNECTION_ID&file=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "file": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fx/latest/actions/get-image-metadata?${params}`, {
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
| `file` | file | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "extension": "string",
        "hasAlpha": true,
        "height": 1,
        "mime": "string",
        "width": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result.extension` | string |  |
| `result.hasAlpha` | boolean |  |
| `result.height` | number |  |
| `result.mime` | string |  |
| `result.width` | number |  |

## Native endpoint

Through the native 1001fx API, this operation is `POST /images/getimagemeta` (base URL `https://api.1001fx.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-image-metadata.md) for the provider-specific parameters and requirements.

