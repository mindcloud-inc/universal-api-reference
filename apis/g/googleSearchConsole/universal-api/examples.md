# Google Search Console Universal API Examples

These examples use the MindCloud API key and Google Search Console connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/list-sites?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/list-sites?${params}`, {
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
      "permissionLevel": "string",
      "siteUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleSearchConsole/latest/actions/list-sites).

## Add Site



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/add-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteUrl": "sc-domain:example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/googleSearchConsole/latest/actions/add-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteUrl": "sc-domain:example.com"
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

See the full [Add Site action reference](actions/add-site.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/googleSearchConsole/latest/actions/add-site).
