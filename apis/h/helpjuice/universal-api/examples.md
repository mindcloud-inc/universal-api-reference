# Helpjuice Universal API Examples

These examples use the MindCloud API key and Helpjuice connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Settings

Retrieves account settings from Helpjuice.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/get-account-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/get-account-settings?${params}`, {
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
      "account": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Account Settings action reference](actions/get-account-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helpjuice/latest/actions/get-account-settings).

## Activate User

Activates a user in Helpjuice.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/activate-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "userId": 1,
  "roleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/helpjuice/latest/actions/activate-user', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "userId": 1,
    "roleId": "string"
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
      "user": {}
    }
  ],
  "meta": {}
}
```

See the full [Activate User action reference](actions/activate-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helpjuice/latest/actions/activate-user).
