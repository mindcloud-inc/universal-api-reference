# TikTok Shop: Search Returns



```
GET https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-returns
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a TikTok Shop `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-returns?connectionId=$CONNECTION_ID&limit=25&offset=0&shopCipher=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "shopCipher": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tikTokShop/latest/actions/search-returns?${params}`, {
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
| `returnIds[]` | array<string> | no |  |
| `orderIds[]` | array<string> | no |  |
| `buyerUserIds[]` | array<string> | no |  |
| `returnTypes` | list<string> | no | One of: `EXCHANGE`, `REFUND`, `REPLACEMENT`, `RETURN_AND_REFUND`. Accepts multiple values as an array. |
| `returnStatus` | list<string> | no | One of: `AWAITING_BUYER_RESPONSE`, `AWAITING_BUYER_SHIP`, `BUYER_SHIPPED_ITEM`, `EXCHANGE_REQUEST_CANCEL`, `EXCHANGE_REQUEST_COMPLETE`, `EXCHANGE_REQUEST_PENDING`, `EXCHANGE_REQUEST_REFUND_SUCCESS`, `REFUND_OR_RETURN_REQUEST_REJECT`, `REJECT_RECEIVE_PACKAGE`, `REPLACEMENT_REQUEST_CANCEL`, `REPLACEMENT_REQUEST_COMPLETE`, `REPLACEMENT_REQUEST_PENDING`, `REPLACEMENT_REQUEST_REFUND_SUCCESS`, `REPLACEMENT_REQUEST_REJECT`, `RETURN_OR_REFUND_REQUEST_CANCEL`, `RETURN_OR_REFUND_REQUEST_COMPLETE`, `RETURN_OR_REFUND_REQUEST_PENDING`, `RETURN_OR_REFUND_REQUEST_SUCCESS`. Accepts multiple values as an array. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `sellerProposedReturnType` | list<string> | no | One of: `PARTIAL_REFUND`. Accepts multiple values as an array. |
| `arbitrationStatus` | list<string> | no | One of: `CLOSED`, `IN_PROGRESS`, `SUPPORT_BUYER`, `SUPPORT_SELLER`. Accepts multiple values as an array. |
| `createTimeGe` | date | no |  |
| `createTimeLt` | date | no |  |
| `updateTimeGe` | date | no |  |
| `updateTimeLt` | date | no |  |
| `locale` | string | no | Default: `en`. |
| `sortField` | list<string> | no | One of: `create_time`, `update_time`. Default: `create_time`. |
| `sortOrder` | list<string> | no | One of: `ASC`, `DESC`. Default: `ASC`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native TikTok Shop API returns.

## Native endpoint

Through the native TikTok Shop API, this operation is `POST /return_refund/202602/returns/search` (base URL `https://open-api.tiktokglobalshop.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/search-returns.md) for the provider-specific parameters and requirements.

