# Scanova Universal API Examples

These examples use the MindCloud API key and Scanova connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Account Statistics



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/account-statistics?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scanova/latest/actions/account-statistics?${params}`, {
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
      "custom_domain_count": 1,
      "dynamic_qr_count": 1,
      "lead_list_count": 1,
      "shared_user_count": 1,
      "static_qr_count": 1,
      "total_designer_qr_count": 1,
      "total_qr_count": 1,
      "total_scan_count": 1
    }
  ],
  "meta": {}
}
```

See the full [Account Statistics action reference](actions/account-statistics.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scanova/latest/actions/account-statistics).

## Add New User



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/scanova/latest/actions/add-new-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "email": "ava@example.com",
  "accessLevel": "1"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/scanova/latest/actions/add-new-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "email": "ava@example.com",
    "accessLevel": "1"
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
      "access_level": {},
      "created": "2026-05-07T12:00:00.000Z",
      "id": 1,
      "invitation_accepted_on": "2026-05-07T12:00:00.000Z",
      "invitation_sent_on": "2026-05-07T12:00:00.000Z",
      "is_invitation_accepted": true,
      "is_invitation_sent": true,
      "modified": "2026-05-07T12:00:00.000Z",
      "shared_user": {},
      "tags": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [Add New User action reference](actions/add-new-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/scanova/latest/actions/add-new-user).
