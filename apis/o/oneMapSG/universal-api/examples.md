# OneMap SG Universal API Examples

These examples use the MindCloud API key and OneMap SG connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Theme Status

Retrieves the status of a OneMap SG theme.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/check-theme-status?connectionId=$CONNECTION_ID&queryName=kindergartens&dateTime=2023-06-15T16%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryName": "kindergartens",
  "dateTime": "2023-06-15T16:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/check-theme-status?${params}`, {
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
      "UpdatedFile": true
    }
  ],
  "meta": {}
}
```

See the full [Check Theme Status action reference](actions/check-theme-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneMapSG/latest/actions/check-theme-status).

## Get Auth Token

Creates an authentication token in OneMap SG.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-auth-token" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/oneMapSG/latest/actions/get-auth-token', {
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
      "expiry_timestamp": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Auth Token action reference](actions/get-auth-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/oneMapSG/latest/actions/get-auth-token).
