# Dachser Universal API Examples

These examples use the MindCloud API key and Dachser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Stock

Retrieves stock records from Dachser by article or warehouse.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-stock?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dachser/latest/actions/get-stock?${params}`, {
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
      "articles": [
        {}
      ],
      "responseItems": [
        {}
      ],
      "storageCustomer": {},
      "warehouse": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Stock action reference](actions/get-stock.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dachser/latest/actions/get-stock).

## Create Labels

Creates shipping labels for a shipment in Dachser.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-labels" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "shipment": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dachser/latest/actions/create-labels', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "shipment": {}
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
      "label": [
        "string"
      ],
      "relation": {},
      "ssccs": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Labels action reference](actions/create-labels.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dachser/latest/actions/create-labels).
