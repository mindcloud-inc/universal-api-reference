# NetLicensing Universal API Examples

These examples use the MindCloud API key and NetLicensing connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Products

Finds products in NetLicensing by filter criteria.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/list-products?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/list-products?${params}`, {
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
      "active": "string",
      "apiKeyRole": "string",
      "code": "string",
      "currency": "string",
      "isEu": "string",
      "licenseeNumber": "string",
      "licenseTemplateNumber": "string",
      "licenseType": "string",
      "licensingModel": "string",
      "lists": {},
      "name": "Ava Chen",
      "number": "string",
      "price": "string",
      "productNumber": "string",
      "shopURL": "https://example.com",
      "source": "string",
      "status": "string",
      "tokenType": "string",
      "type": "string",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Products action reference](actions/list-products.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/netLicensing/latest/actions/list-products).

## Create Bundle

Creates a new bundle in NetLicensing.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/create-bundle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/netLicensing/latest/actions/create-bundle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "active": "string",
      "currency": "string",
      "description": "string",
      "licenseTemplatesNumbers": "string",
      "lists": {},
      "name": "Ava Chen",
      "number": "string",
      "price": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Bundle action reference](actions/create-bundle.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/netLicensing/latest/actions/create-bundle).
