# Microsoft Dynamics 365 Sales Universal API Examples

These examples use the MindCloud API key and Microsoft Dynamics 365 Sales connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/get-current-user?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftDynamics365Sales/latest/actions/get-current-user).

## Update Account



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-account" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "00000000-0000-0000-0000-000000000001"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/microsoftDynamics365Sales/latest/actions/update-account', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "00000000-0000-0000-0000-000000000001"
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

See the full [Update Account action reference](actions/update-account.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/microsoftDynamics365Sales/latest/actions/update-account).
