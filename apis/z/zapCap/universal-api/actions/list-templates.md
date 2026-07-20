# ZapCap: List Templates

Retrieves available templates from ZapCap.

```
GET https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ZapCap `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zapCap/latest/actions/list-templates?${params}`, {
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
      "categories": [
        "string"
      ],
      "id": "string",
      "name": "Ava Chen",
      "previews": {
        "previewGif": "string",
        "previewMp4": "string"
      },
      "previewUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `categories[]` | string |  |
| `id` | string |  |
| `name` | string |  |
| `previews.previewGif` | string |  |
| `previews.previewMp4` | string |  |
| `previewUrl` | string |  |

## Native endpoint

Through the native ZapCap API, this operation is `GET /templates` (base URL `https://api.zapcap.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

