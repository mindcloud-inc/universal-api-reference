# Shopper Approved: Get Review

Retrieves a review from Shopper Approved by ID.

```
GET https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopper Approved `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-review?connectionId=$CONNECTION_ID&reviewId=12345" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "reviewId": "12345"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/get-review?${params}`, {
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
| `reviewId` | string | yes | The review ID or order ID. Example: `12345`. |
| `removed` | number | no | Whether to include removed reviews. Example: `1`. |
| `fullName` | number | no | Whether to include the reviewer's full last name. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopper Approved API returns.

## Native endpoint

Through the native Shopper Approved API, this operation is `GET /reviews/:siteid/:reviewid` (base URL `https://api.shopperapproved.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-review.md) for the provider-specific parameters and requirements.

