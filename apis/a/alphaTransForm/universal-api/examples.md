# Alpha TransForm Universal API Examples

These examples use the MindCloud API key and Alpha TransForm connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Status

Retrieves account status from Alpha TransForm.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-account-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/get-account-status?${params}`, {
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
      "accountDisplayName": "Ava Chen",
      "accountName": "Ava Chen",
      "dateCreated": "string",
      "daysRemaining": 1,
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Status action reference](actions/get-account-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/alphaTransForm/latest/actions/get-account-status).

## Add User To Account

Adds a user to an Alpha TransForm account.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/add-user-to-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/alphaTransForm/latest/actions/add-user-to-account', {
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
  "data": [],
  "meta": {}
}
```

See the full [Add User To Account action reference](actions/add-user-to-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/alphaTransForm/latest/actions/add-user-to-account).
