# Makeswift Universal API Examples

These examples use the MindCloud API key and Makeswift connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Sites

Retrieves sites from Makeswift.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/list-sites?connectionId=$CONNECTION_ID&limit=25&offset=0&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/list-sites?${params}`, {
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
      "data": [
        {}
      ],
      "hasMore": true,
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Sites action reference](actions/list-sites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/makeswift/latest/actions/list-sites).

## Create Locale

Creates a new locale for a site in Makeswift.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/create-locale" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "siteId": "string",
  "locale": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeswift/latest/actions/create-locale', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "siteId": "string",
    "locale": "string"
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
      "domain": "string",
      "id": "string",
      "isDefault": true,
      "locale": "string",
      "object": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Locale action reference](actions/create-locale.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/makeswift/latest/actions/create-locale).
