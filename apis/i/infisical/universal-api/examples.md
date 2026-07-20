# Infisical Universal API Examples

These examples use the MindCloud API key and Infisical connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Folder By ID

Retrieves a folder from Infisical by ID.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/infisical/latest/actions/get-folder-by-id?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/infisical/latest/actions/get-folder-by-id?${params}`, {
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

See the full [Get Folder By ID action reference](actions/get-folder-by-id.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/infisical/latest/actions/get-folder-by-id).

## Authenticate

Authenticates with Infisical using Universal Auth.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/infisical/latest/actions/authenticate" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "clientId": "{{credentials.clientId}}",
  "clientSecret": "{{credentials.clientSecret}}"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/infisical/latest/actions/authenticate', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "clientId": "{{credentials.clientId}}",
    "clientSecret": "{{credentials.clientSecret}}"
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

See the full [Authenticate action reference](actions/authenticate.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/infisical/latest/actions/authenticate).
