# TikTok Shop: Search Return Merchandise Authorizations



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-return-merchandise-authorizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-return-merchandise-authorizations?connectionId=$CONNECTION_ID&limit=25&offset=0&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-return-merchandise-authorizations?${params}`, {
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
| `whitelistedDataFields` | list<string> | no | One of: `LINE_ITEMS`, `SKU_RETURN_REQUESTS`. Accepts multiple values as an array. |
| `filters` | object | no |  |
| `filters.rmaIds[]` | array<string> | no |  |
| `filters.packageIds[]` | array<string> | no |  |
| `filters.statuses` | list<string> | no | One of: `AWAITING_BUYER_RETURN`, `INIT`, `PACKAGE_REVIEW_COMPLETED`, `PENDING_PACKAGE_REVIEW`, `RETURN_IN_TRANSIT`. Accepts multiple values as an array. |
| `filters.aftersalesRequestIds[]` | array<string> | no |  |
| `filters.mainOrderIds[]` | array<string> | no |  |
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

Through the native TikTok Shop API, this operation is `POST /return_refund/202604/rma/search` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-return-merchandise-authorizations.md) for the provider-specific parameters and requirements.

