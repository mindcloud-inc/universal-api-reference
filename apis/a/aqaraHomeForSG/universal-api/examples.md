# Aqara Home for SG Universal API Examples

These examples use the MindCloud API key and Aqara Home for SG connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Access Token

Obtains an access token from Aqara Home for SG.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/get-access-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "authCode": "string",
  "account": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/aqaraHomeForSG/latest/actions/get-access-token', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "authCode": "string",
    "account": "string"
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
      "accessToken": "string",
      "expiresIn": "string",
      "openId": "string",
      "refreshToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Access Token action reference](actions/get-access-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/aqaraHomeForSG/latest/actions/get-access-token).
