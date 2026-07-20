# Fluxguard Universal API Examples

These examples use the MindCloud API key and Fluxguard connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Data

Retrieves your Fluxguard account attributes.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-account-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/get-account-data?${params}`, {
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
      "created": 1,
      "credits": 1,
      "flags": {},
      "id": "string",
      "lastFreeCredits": 1,
      "lastTouch": 1,
      "notifyGap": 1,
      "plan": 1,
      "siteCount": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Data action reference](actions/get-account-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fluxguard/latest/actions/get-account-data).

## Add Page

Adds a new page for monitoring in Fluxguard.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/add-page" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fluxguard/latest/actions/add-page', {
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
  "data": [
    {
      "pageId": "string",
      "sessionId": "string",
      "siteId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Page action reference](actions/add-page.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fluxguard/latest/actions/add-page).
