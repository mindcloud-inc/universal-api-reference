# PageVitals Universal API Examples

These examples use the MindCloud API key and PageVitals connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Websites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-websites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-websites?${params}`, {
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
      "displayName": "Ava Chen",
      "domain": "string",
      "id": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Websites action reference](actions/list-websites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pageVitals/latest/actions/list-websites).

## Add Settings Pages



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/add-settings-pages" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "websiteId": "string",
  "input[].url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/add-settings-pages', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "websiteId": "string",
    "input[].url": "https://example.com"
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
      "alias": "string",
      "id": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Settings Pages action reference](actions/add-settings-pages.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/pageVitals/latest/actions/add-settings-pages).
