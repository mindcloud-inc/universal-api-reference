# GrowthBook: Get list of all code references for the current organization

Retrieves code references from your GrowthBook organization.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-code-refs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-code-refs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/list-code-refs?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "codeRefs": [
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
| `codeRefs` | array<object> |  |
| `count` | number |  |
| `hasMore` | boolean |  |
| `limit` | number |  |
| `nextOffset` | number |  |
| `offset` | number |  |
| `total` | number |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /code-refs` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-code-refs.md) for the provider-specific parameters and requirements.

