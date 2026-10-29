# TikTok Shop: Search Aftersales Requests



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-aftersales-requests
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-aftersales-requests?connectionId=$CONNECTION_ID&limit=25&offset=0&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-aftersales-requests?${params}`, {
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
| `shopCipher` | string | yes |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `locale` | string | no | Default: `en`. |
| `whitelistedDataFields` | list<string> | no | One of: `LINE_ITEMS`, `RETURN_MERCHANDISE_AUTHORIZATIONS`, `SKU_RETURN_REQUESTS`. Accepts multiple values as an array. |
| `filters` | object | no |  |
| `filters.aftersalesRequestIds[]` | array<string> | no |  |
| `filters.aftersalesRequestStatuses` | list<string> | no | One of: `INIT`, `PENDING_REQUEST_REVIEW`, `REQUEST_REVIEW_COMPLETED`. Accepts multiple values as an array. |
| `filters.returnTypes` | list<string> | no | One of: `EXCHANGE`, `REFUND`, `REPLACEMENT`, `RETURN_AND_REFUND`. Accepts multiple values as an array. |
| `filters.mainOrderIds[]` | array<string> | no |  |
| `filters.buyerIds[]` | array<string> | no |  |
| `filters.time` | object | no |  |
| `filters.time.createTime` | object | no |  |
| `filters.time.createTime.minUnixTimeInclusive` | date | no |  |
| `filters.time.createTime.maxUnixTimeExclusive` | date | no |  |
| `filters.time.updateTime` | object | no |  |
| `filters.time.updateTime.minUnixTimeInclusive` | date | no |  |
| `filters.time.updateTime.maxUnixTimeExclusive` | date | no |  |
| `sort` | object | no |  |
| `sort.sortField` | list<string> | no | One of: `CREATE_TIME`, `UPDATE_TIME`. |
| `sort.sortOrder` | list<string> | no | One of: `ASC`, `DESC`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST /return_refund/202603/aftersales/search` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-aftersales-requests.md) for the provider-specific parameters and requirements.

