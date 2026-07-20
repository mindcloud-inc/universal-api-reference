# Bitport Universal API Examples

These examples use the MindCloud API key and Bitport connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the currently authenticated Bitport user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bitport/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bitport/latest/actions/get-current-user?${params}`, {
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

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitport/latest/actions/get-current-user).

## Get Access Token

Creates a Bitport access token from an access code.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/bitport/latest/actions/get-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/bitport/latest/actions/get-access-token', {
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
  "data": [
    {
      "access_token": "string",
      "expires_in": 1,
      "token_type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Access Token action reference](actions/get-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/bitport/latest/actions/get-access-token).
