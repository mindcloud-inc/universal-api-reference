# Influencers.club: Search Creators (Discovery)

Finds creators in Influencers.club by platform-specific discovery filters.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/search-creators-discovery
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/search-creators-discovery?connectionId=$CONNECTION_ID&platform=instagram&limit=2&page=0&aiSearch=fashion%20creators" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "platform": "instagram",
  "limit": "2",
  "page": "0",
  "aiSearch": "fashion creators"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/search-creators-discovery?${params}`, {
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
| `platform` | string | yes | Creator platform to query (e.g., instagram). Default: `instagram`. |
| `limit` | number | yes | Page size for discovery results. Default: `2`. |
| `page` | number | yes | 0-indexed page number. Default: `0`. |
| `aiSearch` | string | yes | Natural-language discovery query. Default: `fashion creators`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sortBy` | string | no | Field used for sorting. Default: `relevancy`. |
| `sortOrder` | string | no | Sort direction (asc or desc). Default: `desc`. |
| `verifiedOnly` | boolean | no | Only include verified creators when true. |
| `minFollowers` | number | no | Minimum follower count filter. |
| `maxFollowers` | number | no | Maximum follower count filter. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accounts": [
        {}
      ],
      "credits_cost": 1,
      "credits_left": 1,
      "limit": 1,
      "total": 1,
      "trial_searches_left": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accounts` | array<object> | Creator account rows matching the query filters. |
| `credits_cost` | number | Credits consumed by this request. |
| `credits_left` | number | Remaining credits after this request. |
| `limit` | number | Page size returned by this response. |
| `total` | number | Total matching creators for the query. |
| `trial_searches_left` | number | Remaining trial searches available. |

## Native endpoint

Through the native Influencers.club API, this operation is `POST /public/v1/discovery/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-creators-discovery.md) for the provider-specific parameters and requirements.

