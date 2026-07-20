# Revel Digital Universal API Examples

These examples use the MindCloud API key and Revel Digital connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Details



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/get-account-details?${params}`, {
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
      "address_1": "string",
      "address_2": "string",
      "business_name": "Ava Chen",
      "city": "string",
      "country": "string",
      "created_on": "string",
      "fax": "string",
      "id": "string",
      "logo_url": "https://example.com",
      "name": "Ava Chen",
      "phone": "string",
      "postal_code": "string",
      "primary_contact_id": "string",
      "secondary_contact_id": "string",
      "state": "string",
      "tags": "string",
      "timeZone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Details action reference](actions/get-account-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/revelDigital/latest/actions/get-account-details).

## Create Data Table



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/create-data-table" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/revelDigital/latest/actions/create-data-table', {
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
      "cacheTtlSeconds": 1,
      "columns": [
        {}
      ],
      "createdAt": "string",
      "description": "string",
      "groupId": "string",
      "id": "string",
      "name": "Ava Chen",
      "rowCount": 1,
      "updatedAt": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Data Table action reference](actions/create-data-table.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/revelDigital/latest/actions/create-data-table).
