# Bland AI: List Pathway Versions

Retrieves pathway versions from Bland AI.

```
GET https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/list-pathway-versions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bland AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/list-pathway-versions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/blandAI/latest/actions/list-pathway-versions?${params}`, {
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
      "created_at": "string",
      "id": "string",
      "is_latest": true,
      "name": "Ava Chen",
      "version_number": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | string |  |
| `is_latest` | boolean |  |
| `name` | string |  |
| `version_number` | number |  |

## Native endpoint

Through the native Bland AI API, this operation is `GET /v1/pathway/{pathway_id}/versions` (base URL `https://api.bland.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-pathway-versions.md) for the provider-specific parameters and requirements.

