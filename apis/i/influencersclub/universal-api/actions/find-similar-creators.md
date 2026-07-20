# Influencers.club: Find Similar Creators

Finds creators similar to a reference creator in Influencers.club.

```
GET https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/find-similar-creators
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Influencers.club `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/find-similar-creators?connectionId=$CONNECTION_ID&filterKey=string&filterValue=string&limit=1&page=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "filterKey": "string",
  "filterValue": "string",
  "limit": "1",
  "page": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/influencersclub/latest/actions/find-similar-creators?${params}`, {
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
| `filterKey` | string | yes | Field key to match for similar creators. |
| `filterValue` | string | yes | Field value to match for similar creators. |
| `limit` | number | yes | Page size for similar creators response. |
| `page` | number | yes | 0-indexed page number. |

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
| `accounts` | array<object> | Creator rows returned by the query. |
| `credits_cost` | number | Credits consumed by this request. |
| `credits_left` | number | Remaining account credits after this request. |
| `limit` | number | Page size returned by this response. |
| `total` | number | Total matching creators for the similarity query. |
| `trial_searches_left` | number | Remaining trial searches available. |

## Native endpoint

Through the native Influencers.club API, this operation is `POST /public/v1/discovery/creators/similar/` (base URL `https://api-dashboard.influencers.club`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/find-similar-creators.md) for the provider-specific parameters and requirements.

