# GrowthBook: Get all sdk connections

Retrieves SDK connections from your GrowthBook organization.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-sdk-connections
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-sdk-connections?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-sdk-connections?${params}`, {
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
| `limit` | number | no | The number of items to return |
| `offset` | number | no | How many items to skip (use in conjunction with limit for pagination) |
| `projectId` | string | no | Filter by project id |
| `withProxy` | string | no |  |
| `multiOrg` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "connections": [
        {}
      ],
      "count": 1,
      "hasMore": true,
      "limit": 1,
      "nextOffset": 1,
      "offset": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `connections` | array<object> |  |
| `count` | number |  |
| `hasMore` | boolean |  |
| `limit` | number |  |
| `nextOffset` | number |  |
| `offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /sdk-connections` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-sdk-connections.md) for the provider-specific parameters and requirements.

