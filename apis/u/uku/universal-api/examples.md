# Uku Universal API Examples

These examples use the MindCloud API key and Uku connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Clients

Retrieves clients from Uku.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-clients?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-clients?${params}`, {
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
      "account_id": 1,
      "address_country_code": "string",
      "billing_settings": {},
      "client_initials": "string",
      "contacts": [
        {}
      ],
      "created_at": "string",
      "default_person_id": 1,
      "fields": {},
      "groups": [
        {}
      ],
      "id": 1,
      "locale_code": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Clients action reference](actions/list-clients.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uku/latest/actions/list-clients).

## Create Client

Creates a new client in Uku.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/uku/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addressCountryCode": "string",
  "clientInitials": "string",
  "name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/uku/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addressCountryCode": "string",
    "clientInitials": "string",
    "name": "Ava Chen"
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
      "account_id": 1,
      "address_country_code": "string",
      "billing_settings": {},
      "client_initials": "string",
      "contacts": [
        {}
      ],
      "created_at": "string",
      "default_person_id": 1,
      "fields": {},
      "groups": [
        {}
      ],
      "id": 1,
      "locale_code": "string",
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/uku/latest/actions/create-client).
