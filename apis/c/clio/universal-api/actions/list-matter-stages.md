# Clio Manage: List Matter Stages

Retrieves matter stages from Clio Manage.

```
GET https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-matter-stages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Clio Manage `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-matter-stages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/clio/latest/actions/list-matter-stages?${params}`, {
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
      "etag": "string",
      "id": 1,
      "name": "Ava Chen",
      "order": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `etag` | string | ETag for the MatterStage. |
| `id` | number | Unique identifier for the MatterStage. |
| `name` | string | The name of the MatterStage. |
| `order` | number | The order of the matter stage within a practice area. |

## Native endpoint

Through the native Clio Manage API, this operation is `GET /matter_stages.json` (base URL `https://app.clio.com/api/v4`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-matter-stages.md) for the provider-specific parameters and requirements.

