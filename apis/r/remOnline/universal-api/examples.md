# RemOnline Universal API Examples

These examples use the MindCloud API key and RemOnline connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Settings

Retrieves your company settings from RemOnline.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/get-company-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/get-company-settings?${params}`, {
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
      "success": true,
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company Settings action reference](actions/get-company-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remOnline/latest/actions/get-company-settings).

## Create Organization

Creates a new organization in RemOnline.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/create-organization" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "MindCloud Stage3 Organization"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remOnline/latest/actions/create-organization', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "MindCloud Stage3 Organization"
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
      "address": "string",
      "business_registration_number": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "custom_fields": {},
      "discount_code": "string",
      "email": "ava@example.com",
      "id": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "notes": "string",
      "phones": [
        {}
      ],
      "supplier": true,
      "tags": [
        "string"
      ],
      "tax_identification_number": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Organization action reference](actions/create-organization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remOnline/latest/actions/create-organization).
