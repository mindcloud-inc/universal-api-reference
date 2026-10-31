# Bridgit Bench Universal API Examples

These examples use the MindCloud API key and Bridgit Bench connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Accounts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-accounts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/list-accounts?${params}`, {
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

See the full [List Accounts action reference](actions/list-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bridgitBench/latest/actions/list-accounts).

## Create Account Certification



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-account-certification" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": 1,
  "name": "Ava Chen",
  "abbreviation": "string",
  "requireExpiration": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bridgitBench/latest/actions/create-account-certification', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": 1,
    "name": "Ava Chen",
    "abbreviation": "string",
    "requireExpiration": true
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

See the full [Create Account Certification action reference](actions/create-account-certification.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bridgitBench/latest/actions/create-account-certification).
