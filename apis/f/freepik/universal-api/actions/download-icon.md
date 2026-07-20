# Freepik: Download Icon

Retrieves a Freepik icon download URL.

```
GET https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-icon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freepik `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-icon?connectionId=$CONNECTION_ID&id=4326138" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "4326138"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freepik/latest/actions/download-icon?${params}`, {
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
| `id` | number | yes | Freepik icon identifier to download. Default: `4326138`. |
| `format` | list | no | Icon download format. PNG is verified with the current credential. One of: `png`. Default: `png`. |
| `pngSize` | number | no | PNG size in pixels when format is png. Default: `512`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "filename": "Ava Chen",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `filename` | string | Icon download filename. |
| `url` | string | Icon download URL. |

## Native endpoint

Through the native Freepik API, this operation is `GET /v1/icons/{{id}}/download` (base URL `https://api.freepik.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-icon.md) for the provider-specific parameters and requirements.

