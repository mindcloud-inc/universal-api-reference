# Globalping Universal API Examples

These examples use the MindCloud API key and Globalping connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Limits

Retrieves current Globalping usage limits.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-limits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/globalping/latest/actions/get-limits?${params}`, {
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
      "credits": {},
      "rateLimit": {}
    }
  ],
  "meta": {}
}
```

See the full [Get Limits action reference](actions/get-limits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/globalping/latest/actions/get-limits).

## Create DNS A Measurement

Creates a DNS A measurement in Globalping.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/globalping/latest/actions/create-dns-a-measurement" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "target": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/globalping/latest/actions/create-dns-a-measurement', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "target": "string"
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
      "id": "string",
      "probesCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Create DNS A Measurement action reference](actions/create-dns-a-measurement.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/globalping/latest/actions/create-dns-a-measurement).
