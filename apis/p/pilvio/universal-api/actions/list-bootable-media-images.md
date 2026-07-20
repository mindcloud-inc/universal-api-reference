# Pilvio: List Bootable Media Images



```
GET https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-bootable-media-images
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pilvio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-bootable-media-images?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pilvio/latest/actions/list-bootable-media-images?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "description": "string",
      "imageName": "Ava Chen",
      "isInstallationMedia": true,
      "isPublished": true,
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `description` | string |  |
| `imageName` | string |  |
| `isInstallationMedia` | boolean |  |
| `isPublished` | boolean |  |
| `uuid` | string |  |

## Native endpoint

Through the native Pilvio API, this operation is `GET /config/boot_images` (base URL `https://api.pilvio.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bootable-media-images.md) for the provider-specific parameters and requirements.

