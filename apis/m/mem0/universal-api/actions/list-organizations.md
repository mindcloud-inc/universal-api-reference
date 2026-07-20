# Mem0: List Organizations

Retrieves organizations from Mem0.

```
GET https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mem0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mem0/latest/actions/list-organizations?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `description` | string |  |
| `id` | string |  |
| `name` | string |  |

## Native endpoint

Through the native Mem0 API, this operation is `GET /api/v1/orgs/organizations/` (base URL `https://api.mem0.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

