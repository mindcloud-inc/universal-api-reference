# Vtiger CRM Universal API Examples

These examples use the MindCloud API key and Vtiger CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user profile from Vtiger CRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/get-current-user?${params}`, {
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
      "email1": "ava@example.com",
      "first_name": "Ava",
      "id": "string",
      "is_admin": "string",
      "last_name": "Chen",
      "user_name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vtigerCRM/latest/actions/get-current-user).

## Create Account

Creates a new account in Vtiger CRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "element": {
    "accountname": "Stage3 Default Account"
  }
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vtigerCRM/latest/actions/create-account', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "element": {"accountname":"Stage3 Default Account"}
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
      "id": "string",
      "label": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Account action reference](actions/create-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vtigerCRM/latest/actions/create-account).
