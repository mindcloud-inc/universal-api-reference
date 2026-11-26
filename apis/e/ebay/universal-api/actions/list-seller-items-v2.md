# eBay: List Seller Items_v2

Retrieve items listed by the authenticated user, including item data.

```
GET https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-seller-items-v2
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a eBay `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-seller-items-v2?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ebay/latest/actions/list-seller-items-v2?${params}`, {
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
| `startTimeTo` | date | no |  |
| `startTimeFrom` | date | no |  |
| `skus` | string | no | (SKUArray) Accepts multiple values as an array. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native eBay API returns.

## Native endpoint

Through the native eBay API, this operation is `POST` (base URL `https://api.ebay.com/ws/api.dll`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-seller-items-v2.md) for the provider-specific parameters and requirements.

