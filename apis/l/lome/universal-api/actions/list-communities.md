# Lome: List Communities

Retrieves your hosted communities from Lome.

```
GET https://connect.mindcloud.co/v1/universal/lome/latest/actions/list-communities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lome/latest/actions/list-communities?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lome/latest/actions/list-communities?${params}`, {
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
      "color": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "image": "string",
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `color` | string |  |
| `created_at` | date |  |
| `id` | string |  |
| `image` | string |  |
| `name` | string |  |
| `slug` | string |  |

## Native endpoint

Through the native Lome API, this operation is `GET /v1/communities` (base URL `https://grow.withlome.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-communities.md) for the provider-specific parameters and requirements.

