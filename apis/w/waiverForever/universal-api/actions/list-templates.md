# WaiverForever: List Templates

Retrieves templates from WaiverForever.

```
GET https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-templates
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a WaiverForever `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-templates?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/waiverForever/latest/actions/list-templates?${params}`, {
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
      "createdAt": 1,
      "disabled": true,
      "id": "string",
      "tags": [
        "string"
      ],
      "title": "string",
      "updatedAt": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | number | Template creation timestamp. |
| `disabled` | boolean | Whether the template is disabled. |
| `id` | string | Template id. |
| `tags` | array<string> | Template tags. |
| `title` | string | Template title. |
| `updatedAt` | number | Template update timestamp. |

## Native endpoint

Through the native WaiverForever API, this operation is `GET /openapi/v1/templates` (base URL `https://api.waiverforever.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-templates.md) for the provider-specific parameters and requirements.

