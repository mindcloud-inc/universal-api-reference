# Invoice Ninja Universal API Examples

These examples use the MindCloud API key and Invoice Ninja connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Payment Terms



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-payment-terms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/list-payment-terms?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Payment Terms action reference](actions/list-payment-terms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invoiceNinja/latest/actions/list-payment-terms).

## Bulk Client Actions



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-client-actions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "action": "string",
  "ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/invoiceNinja/latest/actions/bulk-client-actions', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "action": "string",
    "ids[]": ["string"]
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
      "balance": 1,
      "contacts": [
        {}
      ],
      "country_id": "string",
      "created_at": 1,
      "display_name": "Ava Chen",
      "documents": [
        {}
      ],
      "has_valid_vat_number": true,
      "id": "string",
      "is_deleted": true,
      "is_tax_exempt": true,
      "locations": [
        {}
      ],
      "name": "Ava Chen",
      "number": "string",
      "public_notes": "string",
      "settings": {},
      "updated_at": 1
    }
  ],
  "meta": {}
}
```

See the full [Bulk Client Actions action reference](actions/bulk-client-actions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/invoiceNinja/latest/actions/bulk-client-actions).
