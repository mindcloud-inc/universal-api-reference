# lemlist Universal API Examples

These examples use the MindCloud API key and lemlist connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Team Credits

Retrieves your team credits from lemlist.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-team-credits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/get-team-credits?${params}`, {
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
      "credits": 1,
      "details": {
        "remaining": {
          "freemium": 1,
          "gifted": 1,
          "paid": 1,
          "subscription": 1,
          "total": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Team Credits action reference](actions/get-team-credits.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lemlist/latest/actions/get-team-credits).

## Add Webhook

Creates a new webhook in lemlist.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/add-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://webhook.site/1d50ac35-2755-42cc-964c-9acbb4ebca30"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/lemlist/latest/actions/add-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://webhook.site/1d50ac35-2755-42cc-964c-9acbb4ebca30"
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
      "createdAt": "string",
      "id": "string",
      "targetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Add Webhook action reference](actions/add-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/lemlist/latest/actions/add-webhook).
