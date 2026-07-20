# Shopper Approved: Update or Cancel Review

Updates or cancels a review in Shopper Approved.

```
PUT https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/update-or-cancel-review
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shopper Approved `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/update-or-cancel-review" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "reviewId": "12345"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/update-or-cancel-review', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "reviewId": "12345"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `reviewId` | string | yes | The review ID or order ID. Example: `12345`. |
| `followup` | date | no | The follow-up date in YYYY-MM-DD format. Example: `2026-03-31`. |
| `cancel` | number | no | Set to 1 to cancel the review. Example: `1`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Shopper Approved API returns.

## Native endpoint

Through the native Shopper Approved API, this operation is `PUT /reviews/:siteid/:reviewid` (base URL `https://api.shopperapproved.com/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-or-cancel-review.md) for the provider-specific parameters and requirements.

