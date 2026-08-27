# Acumatica Universal API Examples

These examples use the MindCloud API key and Acumatica connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Acumatica Endpoints

Retrieve the Acumatica ERP Endpoints and the build version.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-acumatica-erp-endpoints?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/get-acumatica-erp-endpoints?${params}`, {
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
      "endpoints": [
        {
          "href": "string",
          "name": "Ava Chen",
          "version": "string"
        }
      ],
      "version": {
        "acumaticaBuildVersion": "string",
        "databaseVersion": "string"
      }
    }
  ],
  "meta": {}
}
```

See the full [List Acumatica Endpoints action reference](actions/get-acumatica-erp-endpoints.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/acumatica/latest/actions/get-acumatica-erp-endpoints).

## Confirm Shipment



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/confirm-shipment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/confirm-shipment', {
  method: 'PUT',
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
  "data": [],
  "meta": {}
}
```

See the full [Confirm Shipment action reference](actions/confirm-shipment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/acumatica/latest/actions/confirm-shipment).
