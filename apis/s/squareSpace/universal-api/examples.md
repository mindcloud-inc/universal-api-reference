# SquareSpace Universal API Examples

These examples use the MindCloud API key and SquareSpace connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Image Processing Status

Retrieves product image processing status from Squarespace.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-image-processing-status?connectionId=$CONNECTION_ID&imageId=string&productId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "imageId": "string",
  "productId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/get-image-processing-status?${params}`, {
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
  "data": [
    {
      "id": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Image Processing Status action reference](actions/get-image-processing-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/squareSpace/latest/actions/get-image-processing-status).

## Adjust Stock Quantities

Updates stock quantities in Squarespace.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/adjust-stock-quantities" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "idempotencyKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/squareSpace/latest/actions/adjust-stock-quantities', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "idempotencyKey": "string"
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

See the full [Adjust Stock Quantities action reference](actions/adjust-stock-quantities.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/squareSpace/latest/actions/adjust-stock-quantities).
