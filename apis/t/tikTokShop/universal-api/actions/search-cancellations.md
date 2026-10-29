# TikTok Shop: Search Cancellations



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-cancellations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-cancellations?connectionId=$CONNECTION_ID&limit=25&offset=0&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-cancellations?${params}`, {
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
| `cancelTypes` | list<string> | no | One of: `BUYER_CANCEL`, `CANCEL`. Accepts multiple values as an array. |
| `cancelStatus` | list<string> | no | One of: `CANCELLATION_REQUEST_CANCEL`, `CANCELLATION_REQUEST_COMPLETE`, `CANCELLATION_REQUEST_PENDING`, `CANCELLATION_REQUEST_SUCCESS`. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cancelIds[]` | array<string> | no |  |
| `orderIds[]` | array<string> | no |  |
| `buyerUserIds[]` | array<string> | no |  |
| `createTimeGe` | date | no |  |
| `createTimeLt` | date | no |  |
| `updateTimeGe` | date | no |  |
| `updateTimeLt` | date | no |  |
| `locale` | string | no | Default: `en-US`. |
| `sortField` | list<string> | no | One of: `create_time`, `update_time`. Default: `create_time`. |
| `sortOrder` | list<string> | no | One of: `ASC`, `DESC`. Default: `ASC`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST /return_refund/202602/cancellations/search` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-cancellations.md) for the provider-specific parameters and requirements.

