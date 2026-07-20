# Audius Universal API Examples

These examples use the MindCloud API key and Audius connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Developer App

Retrieves a developer app from Audius by address.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/audius/latest/actions/get-developer-app?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/audius/latest/actions/get-developer-app?${params}`, {
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

See the full [Get Developer App action reference](actions/get-developer-app.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/audius/latest/actions/get-developer-app).

## Register API Key

Creates API key credentials for an Audius developer app.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/audius/latest/actions/register-api-key" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/audius/latest/actions/register-api-key', {
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

See the full [Register API Key action reference](actions/register-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/audius/latest/actions/register-api-key).
