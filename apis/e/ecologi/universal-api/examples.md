# Ecologi Universal API Examples

These examples use the MindCloud API key and Ecologi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Total Number of Trees

Retrieves total trees planted from Ecologi.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-number-of-trees?connectionId=$CONNECTION_ID&username=business-name" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "username": "business-name"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/get-total-number-of-trees?${params}`, {
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
      "pending": 1,
      "total": 1
    }
  ],
  "meta": {}
}
```

See the full [Get Total Number of Trees action reference](actions/get-total-number-of-trees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ecologi/latest/actions/get-total-number-of-trees).

## Purchase Carbon Avoidance

Purchases carbon avoidance through Ecologi.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/purchase-carbon-avoidance" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "number": "10",
  "units": "KG"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ecologi/latest/actions/purchase-carbon-avoidance', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "number": "10",
    "units": "KG"
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

See the full [Purchase Carbon Avoidance action reference](actions/purchase-carbon-avoidance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ecologi/latest/actions/purchase-carbon-avoidance).
