# Hyperbrowser Universal API Examples

These examples use the MindCloud API key and Hyperbrowser connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Fetch Web Page



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/fetch-web-page?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/fetch-web-page?${params}`, {
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
      "data": {},
      "jobId": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Fetch Web Page action reference](actions/fetch-web-page.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperbrowser/latest/actions/fetch-web-page).

## Create Profile



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/create-profile" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/hyperbrowser/latest/actions/create-profile', {
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
      "id": "string",
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Create Profile action reference](actions/create-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/hyperbrowser/latest/actions/create-profile).
