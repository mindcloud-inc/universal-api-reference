# Fraser Direct Universal API Examples

These examples use the MindCloud API key and Fraser Direct connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get inventory



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory?connectionId=$CONNECTION_ID&groupByLot=N&includeInPick=N" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "groupByLot": "N",
  "includeInPick": "N"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/get-inventory?${params}`, {
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
      "groupByLot": "string",
      "includeInPick": "string",
      "inventoryItems": [
        {}
      ],
      "recordCount": 1,
      "success": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get inventory action reference](actions/get-inventory.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fraserDirect/latest/actions/get-inventory).

## Create order



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/create-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stName": "Ava Chen",
  "stAddress1": "string",
  "stCity": "string",
  "stProvince": "string",
  "stPostalCode": "string",
  "stCountry": "string",
  "poDate": "2024-11-06",
  "serviceLevel": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fraserDirect/latest/actions/create-order', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stName": "Ava Chen",
    "stAddress1": "string",
    "stCity": "string",
    "stProvince": "string",
    "stPostalCode": "string",
    "stCountry": "string",
    "poDate": "2024-11-06",
    "serviceLevel": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "orderNumber": "string",
      "orderStatus": "string",
      "po": "string",
      "success": "string",
      "validationResults": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create order action reference](actions/create-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fraserDirect/latest/actions/create-order).
