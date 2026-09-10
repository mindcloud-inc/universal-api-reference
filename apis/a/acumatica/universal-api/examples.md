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

## Cancel Sales Order



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/cancel-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entity.OrderType.value": "string",
  "entity.OrderNbr.value": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/acumatica/latest/actions/cancel-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entity.OrderType.value": "string",
    "entity.OrderNbr.value": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Cancel Sales Order action reference](actions/cancel-sales-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/acumatica/latest/actions/cancel-sales-order).
