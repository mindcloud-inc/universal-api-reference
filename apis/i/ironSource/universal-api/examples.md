# ironSource Universal API Examples

These examples use the MindCloud API key and ironSource connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Bearer Token

Retrieves a bearer token from ironSource.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-bearer-token?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/get-bearer-token?${params}`, {
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
      "accessToken": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Bearer Token action reference](actions/get-bearer-token.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ironSource/latest/actions/get-bearer-token).

## Create Ad Units

Creates new ad units in ironSource.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/create-ad-units" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ironSource/latest/actions/create-ad-units', {
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Ad Units action reference](actions/create-ad-units.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ironSource/latest/actions/create-ad-units).
