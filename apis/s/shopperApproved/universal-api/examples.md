# Shopper Approved Universal API Examples

These examples use the MindCloud API key and Shopper Approved connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Reviews

Retrieves reviews from Shopper Approved.

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

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [List Reviews action reference](actions/list-reviews.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shopperApproved/latest/actions/list-reviews).

## Create Review Entry

Creates a new review entry in Shopper Approved.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/create-review-entry" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "customer@example.com",
  "followup": "2026-03-31",
  "orderId": "ORDER-1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shopperApproved/latest/actions/create-review-entry', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "customer@example.com",
    "followup": "2026-03-31",
    "orderId": "ORDER-1001"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Create Review Entry action reference](actions/create-review-entry.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/shopperApproved/latest/actions/create-review-entry).
