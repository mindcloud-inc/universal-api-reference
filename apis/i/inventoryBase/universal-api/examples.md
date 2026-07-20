# InventoryBase Universal API Examples

These examples use the MindCloud API key and InventoryBase connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user profile from InventoryBase.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/get-current-user?${params}`, {
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
      "accountId": 1,
      "accountSettings": {},
      "company": "string",
      "currencyCode": "string",
      "currencySymbol": "string",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "role": 1,
      "signature": "string",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inventoryBase/latest/actions/get-current-user).

## Create Client

Creates a new client in InventoryBase.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-client" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com",
  "address": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/inventoryBase/latest/actions/create-client', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com",
    "address": {}
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
      "additionalEmails": [
        "ava@example.com"
      ],
      "address": {
        "city": "string",
        "country": "string",
        "county": "string",
        "line1": "string",
        "line2": "string",
        "postcode": "string"
      },
      "billingEmail": "ava@example.com",
      "company": "string",
      "companyNo": "string",
      "createdAt": "string",
      "customFields": {},
      "deletedAt": "string",
      "disabledTypes": [
        "string"
      ],
      "email": "ava@example.com",
      "emailNotifications": true,
      "id": 1,
      "isAdminManager": true,
      "isManager": true,
      "isTypist": true,
      "loginEnabled": true,
      "logo": "string",
      "mobile": "string",
      "name": "Ava Chen",
      "notes": "string",
      "pendingEmail": "ava@example.com",
      "role": 1,
      "settings": {},
      "signature": "string",
      "telephone": "string",
      "title": "string",
      "vatNo": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Client action reference](actions/create-client.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/inventoryBase/latest/actions/create-client).
