# SimpliRoute Universal API Examples

These examples use the MindCloud API key and SimpliRoute connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account

Retrieves the authenticated account from SimpliRoute.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/get-account?${params}`, {
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
      "account": {},
      "blocked": true,
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "gps_config": {},
      "has_suscription_id": true,
      "id": 1,
      "is_admin": true,
      "is_codriver": true,
      "is_coordinator": true,
      "is_driver": true,
      "is_monitor": true,
      "is_owner": true,
      "is_router": true,
      "is_router_jr": true,
      "is_seller": true,
      "is_seller_viewer": true,
      "is_staff": true,
      "last_login": "2026-05-07T12:00:00.000Z",
      "modified": "2026-05-07T12:00:00.000Z",
      "modules": [
        {}
      ],
      "name": "Ava Chen",
      "old_id": 1,
      "organization": {},
      "phone": "string",
      "role": {},
      "status": "string",
      "url": "https://example.com",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Account action reference](actions/get-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpliRoute/latest/actions/get-account).

## Create User

Creates a new driver in SimpliRoute.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "password": "string",
  "username": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/simpliRoute/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "password": "string",
    "username": "Ava Chen"
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
      "app_version": "string",
      "blocked": true,
      "created": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "is_admin": true,
      "is_codriver": true,
      "is_coordinator": true,
      "is_driver": true,
      "is_monitor": true,
      "is_owner": true,
      "is_router": true,
      "is_router_jr": true,
      "is_seller": true,
      "is_seller_viewer": true,
      "is_staff": true,
      "last_login": "2026-05-07T12:00:00.000Z",
      "last_mobile_activity": "2026-05-07T12:00:00.000Z",
      "modified": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "old_id": 1,
      "phone": "string",
      "status": "string",
      "username": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create User action reference](actions/create-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/simpliRoute/latest/actions/create-user).
