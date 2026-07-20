# Urlbox Universal API Examples

These examples use the MindCloud API key and Urlbox connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Check Render Status

Retrieves the status of a render from Urlbox.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/check-render-status?connectionId=$CONNECTION_ID&renderId=250ea007-552c-4555-ba2b-ef1c73e18be2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "renderId": "250ea007-552c-4555-ba2b-ef1c73e18be2"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/check-render-status?${params}`, {
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
      "bandwidth": 1,
      "queueTime": 1,
      "reason": "string",
      "renderId": "string",
      "renderTime": 1,
      "renderUrl": "https://example.com",
      "size": 1,
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Check Render Status action reference](actions/check-render-status.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/urlbox/latest/actions/check-render-status).

## Create Asynchronous Render

Creates an asynchronous render in Urlbox.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/create-asynchronous-render" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/urlbox/latest/actions/create-asynchronous-render', {
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
      "renderId": "string",
      "status": "string",
      "statusUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Asynchronous Render action reference](actions/create-asynchronous-render.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/urlbox/latest/actions/create-asynchronous-render).
