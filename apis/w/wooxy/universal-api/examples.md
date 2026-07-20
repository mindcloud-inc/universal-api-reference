# Wooxy Universal API Examples

These examples use the MindCloud API key and Wooxy connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves your current Wooxy account information.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/get-account-info?${params}`, {
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
      "accountBalance": 1,
      "accountName": "Ava Chen",
      "result": true
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wooxy/latest/actions/get-account-info).

## Create Account Variable

Creates a new account variable in Wooxy.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-account-variable" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "stageThreeVar",
  "value": "stage three value"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/wooxy/latest/actions/create-account-variable', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "stageThreeVar",
    "value": "stage three value"
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

See the full [Create Account Variable action reference](actions/create-account-variable.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/wooxy/latest/actions/create-account-variable).
