# Flexport Universal API Examples

These examples use the MindCloud API key and Flexport connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Shipments

Retrieves shipments from your Flexport account.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-shipments?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexport/latest/actions/list-shipments?${params}`, {
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
      "airShipment": {},
      "calculatedVolume": {},
      "calculatedWeight": {},
      "cargoReadyDate": "2026-05-07T12:00:00.000Z",
      "consignees": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "dangerousGoods": {},
      "documents": {},
      "freightCost": "string",
      "freightType": "string",
      "id": 1,
      "incoterm": "string",
      "items": [
        {}
      ],
      "legs": {},
      "name": "Ava Chen",
      "oceanShipment": {},
      "pieces": 1,
      "shippers": [
        {}
      ],
      "status": "string",
      "transportationMode": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Shipments action reference](actions/list-shipments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flexport/latest/actions/list-shipments).

## Create Product

Creates a new product in Flexport.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/flexport/latest/actions/create-product" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Organic Cotton T-Shirt",
  "sku": "SKU-1001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/flexport/latest/actions/create-product', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Organic Cotton T-Shirt",
    "sku": "SKU-1001"
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
      "archivedAt": "2026-05-07T12:00:00.000Z",
      "classifications": [
        {}
      ],
      "clientVerified": true,
      "countryOfOrigin": "string",
      "description": "string",
      "hsCodes": [
        {}
      ],
      "id": 1,
      "name": "Ava Chen",
      "productCategory": "string",
      "productProperties": [
        {}
      ],
      "sku": "string",
      "suppliers": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Create Product action reference](actions/create-product.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/flexport/latest/actions/create-product).
