# Screenly: List Assets

Retrieves assets from Screenly.

```
GET https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-assets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-assets?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenly/latest/actions/list-assets?${params}`, {
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
      "assetUrl": "https://example.com",
      "disableVerification": true,
      "duration": 1,
      "finalized": true,
      "height": 1,
      "id": "string",
      "md5": "string",
      "metadata": {},
      "sourceMd5": "string",
      "sourceUrl": "https://example.com",
      "status": "string",
      "title": "string",
      "type": "string",
      "url": "https://example.com",
      "width": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `assetUrl` | string |  |
| `disableVerification` | boolean |  |
| `duration` | number |  |
| `finalized` | boolean |  |
| `height` | number |  |
| `id` | string |  |
| `md5` | string |  |
| `metadata` | object |  |
| `sourceMd5` | string |  |
| `sourceUrl` | string |  |
| `status` | string |  |
| `title` | string |  |
| `type` | string |  |
| `url` | string |  |
| `width` | number |  |

## Native endpoint

Through the native Screenly API, this operation is `GET /assets/` (base URL `https://api.screenlyapp.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-assets.md) for the provider-specific parameters and requirements.

