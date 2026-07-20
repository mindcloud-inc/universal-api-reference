# Vector Vault Universal API Examples

These examples use the MindCloud API key and Vector Vault connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Vaults



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/vectorVault/latest/actions/list-vaults?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/vectorVault/latest/actions/list-vaults?${params}`, {
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

See the full [List Vaults action reference](actions/list-vaults.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vectorVault/latest/actions/list-vaults).

## Authenticate



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/vectorVault/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "{{credentials.email}}",
  "apiKey": "{{credentials.apiKey}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/vectorVault/latest/actions/authenticate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "{{credentials.email}}",
    "apiKey": "{{credentials.apiKey}}"
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
      "access_token": "string",
      "refresh_token": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/vectorVault/latest/actions/authenticate).
