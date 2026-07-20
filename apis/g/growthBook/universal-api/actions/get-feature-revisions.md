# GrowthBook: List revisions for a feature

Retrieves revisions for a GrowthBook feature.

```
GET https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-feature-revisions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GrowthBook `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-feature-revisions?connectionId=$CONNECTION_ID&limit=25&offset=0&id=prj_19g6smo332up7" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "id": "prj_19g6smo332up7"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/growthBook/latest/actions/get-feature-revisions?${params}`, {
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
| `id` | string | yes | The id of the requested resource Default: `prj_19g6smo332up7`. |
| `limit` | number | no | The number of items to return |
| `offset` | number | no | How many items to skip (use in conjunction with limit for pagination) |
| `skipPagination` | string | no | If true, return all matching items and ignore limit/offset. Self-hosted only. Has no effect unless API_ALLOW_SKIP_PAGINATION is set to true or 1. |
| `status` | string | no |  |
| `author` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "hasMore": true,
      "limit": 1,
      "nextOffset": 1,
      "offset": 1,
      "revisions": [
        {}
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `hasMore` | boolean |  |
| `limit` | number |  |
| `nextOffset` | number |  |
| `offset` | number |  |
| `revisions` | array<object> |  |
| `total` | number |  |

## Native endpoint

Through the native GrowthBook API, this operation is `GET /features/:id/revisions` (base URL `https://api.growthbook.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-feature-revisions.md) for the provider-specific parameters and requirements.

