# Teletype App Universal API Examples

These examples use the MindCloud API key and Teletype App connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Project Details

Retrieves project details from Teletype App.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/get-project-details?${params}`, {
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
      "createdAt": {},
      "domain": "string",
      "id": "string",
      "name": "Ava Chen",
      "ownerId": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Project Details action reference](actions/get-project-details.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teletypeApp/latest/actions/get-project-details).

## Update Public API Settings

Updates public API settings in Teletype App.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/update-public-api-settings" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/teletypeApp/latest/actions/update-public-api-settings', {
  method: 'PUT',
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
      "value": true
    }
  ],
  "meta": {}
}
```

See the full [Update Public API Settings action reference](actions/update-public-api-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/teletypeApp/latest/actions/update-public-api-settings).
