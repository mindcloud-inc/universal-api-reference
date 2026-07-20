# Wasi Universal API Examples

These examples use the MindCloud API key and Wasi connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Properties

Finds properties in Wasi by search criteria.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-properties?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wasi/latest/actions/list-properties?${params}`, {
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
      "address": "string",
      "city_label": "string",
      "country_label": "string",
      "for_rent": true,
      "for_sale": true,
      "for_transfer": true,
      "id_city": 1,
      "id_country": 1,
      "id_property": 1,
      "id_property_type": 1,
      "id_region": 1,
      "property_type_label": "string",
      "region_label": "string",
      "rent_price": 1,
      "sale_price": 1,
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Properties action reference](actions/list-properties.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wasi/latest/actions/list-properties).

## Change Property Label

Updates a property label in Wasi.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/wasi/latest/actions/change-property-label" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "label": "codex-test-label",
  "property_id": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wasi/latest/actions/change-property-label', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "label": "codex-test-label",
    "property_id": "1"
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Change Property Label action reference](actions/change-property-label.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wasi/latest/actions/change-property-label).
