# Shopper Approved: List Reviews

Retrieves reviews from Shopper Approved.

```
GET https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopper Approved `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/list-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/list-reviews?${params}`, {
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
| `from` | date | no | The first date in YYYY-MM-DD format. Example: `2026-03-01`. |
| `to` | date | no | The last date in YYYY-MM-DD format. Example: `2026-03-24`. |
| `rating` | string | no | Comma-separated star ratings to include. Default: `1,2,3,4,5`. Example: `5 or 4,5`. |
| `sort` | string | no | How the reviews should be sorted. Example: `newest`. |
| `fullName` | number | no | Whether to include the reviewer's full last name. Example: `1`. |
| `removed` | number | no | Whether to include removed reviews. Example: `1`. |
| `test` | boolean | no | Whether to include reviews marked as test or possible spam. Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopper Approved API returns.

## Native endpoint

Through the native Shopper Approved API, this operation is `GET /reviews/:siteid` (base URL `https://api.shopperapproved.com/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

