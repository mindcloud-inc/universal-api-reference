# Zoho Inventory Universal API Examples

These examples use the MindCloud API key and Zoho Inventory connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from Zoho Inventory.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-organizations?${params}`, {
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
      "country": "string",
      "country_code": "string",
      "currency_code": "string",
      "email": "ava@example.com",
      "is_default_org": true,
      "is_org_active": true,
      "name": "Ava Chen",
      "org_joined_app_list": [
        "string"
      ],
      "organization_id": "string",
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoInventory/latest/actions/list-organizations).

## Confirm Sales Order

Marks a sales order as confirmed in Zoho Inventory.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/confirm-sales-order" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "salesOrderId": "string",
  "organizationId": "{{credentials.organizationId}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/confirm-sales-order', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "salesOrderId": "string",
    "organizationId": "{{credentials.organizationId}}"
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
      "code": 1,
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Confirm Sales Order action reference](actions/confirm-sales-order.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoInventory/latest/actions/confirm-sales-order).
