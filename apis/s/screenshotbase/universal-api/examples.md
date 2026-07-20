# Screenshotbase Universal API Examples

These examples use the MindCloud API key and Screenshotbase connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check API Status

Retrieves current quota status from Screenshotbase.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/check-api-status?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/check-api-status?${params}`, {
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
      "accountId": 1,
      "quotas": {
        "grace": {
          "remaining": 1,
          "total": 1,
          "used": 1
        },
        "month": {
          "remaining": 1,
          "total": 1,
          "used": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Check API Status action reference](actions/check-api-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/screenshotbase/latest/actions/check-api-status).

## Take Website Screenshot

Captures a website screenshot with Screenshotbase.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/take-website-screenshot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/screenshotbase/latest/actions/take-website-screenshot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "url": "https://example.com"
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

See the full [Take Website Screenshot action reference](actions/take-website-screenshot.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/screenshotbase/latest/actions/take-website-screenshot).
