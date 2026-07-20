# Dash.app Universal API Examples

These examples use the MindCloud API key and Dash.app connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Dash.app.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/get-current-user?${params}`, {
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
      "accountId": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastLogin": "2026-05-07T12:00:00.000Z",
      "lastName": "Chen",
      "name": "Ava Chen",
      "permissions": {},
      "picture": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dashapp/latest/actions/get-current-user).

## Create Asset Share

Creates a new asset share in Dash.app.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-asset-share" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "assetIds[]": "7af90a8b-7ccd-430f-a85d-e8614015bc47",
  "expiry": "null"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dashapp/latest/actions/create-asset-share', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "assetIds[]": "7af90a8b-7ccd-430f-a85d-e8614015bc47",
    "expiry": "null"
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
      "permittedActions": [
        {}
      ],
      "result": {}
    }
  ],
  "meta": {}
}
```

See the full [Create Asset Share action reference](actions/create-asset-share.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dashapp/latest/actions/create-asset-share).
