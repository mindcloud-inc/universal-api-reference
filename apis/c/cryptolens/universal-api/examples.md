# Cryptolens Universal API Examples

These examples use the MindCloud API key and Cryptolens connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Retrieves products from Cryptolens.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/list-products?${params}`, {
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
      "creationDate": "string",
      "dataObjects": [
        "string"
      ],
      "description": "string",
      "featureDefinitions": {},
      "id": 1,
      "isPublic": true,
      "keyAlgorithm": 1,
      "name": "Ava Chen",
      "password": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cryptolens/latest/actions/list-products).

## Activate

Activates a license key in Cryptolens.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/activate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "productId": 1,
  "key": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/cryptolens/latest/actions/activate', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "productId": 1,
    "key": "string"
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
      "licenseKey": {},
      "productId": 1
    }
  ],
  "meta": {}
}
```

See the full [Activate action reference](actions/activate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cryptolens/latest/actions/activate).
