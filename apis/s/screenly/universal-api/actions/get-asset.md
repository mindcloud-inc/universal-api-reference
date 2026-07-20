# Screenly: Get Asset

Retrieves an asset from Screenly.

```
GET https://connect.mindcloud.co/v1/universal/screenly/latest/actions/get-asset
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Screenly `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenly/latest/actions/get-asset?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenly/latest/actions/get-asset?${params}`, {
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
| `id` | string | yes |  |

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

Through the native Screenly API, this operation is `GET /assets/:id/` (base URL `https://api.screenlyapp.com/api/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-asset.md) for the provider-specific parameters and requirements.

