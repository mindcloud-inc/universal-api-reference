# Sunwise: Recent Projects

Retrieves recent projects from Sunwise.

```
GET https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/recent-projects
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/recent-projects?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/recent-projects?${params}`, {
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
      "description": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Sunwise API, this operation is `GET /projects/recent-projects/` (base URL `https://production.sunwise.ai/boty/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/recent-projects.md) for the provider-specific parameters and requirements.

