# Beehiiv Universal API Examples

These examples use the MindCloud API key and Beehiiv connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Publications

Retrieves publications from Beehiiv.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publications?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/list-publications?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [List Publications action reference](actions/list-publications.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beehiiv/latest/actions/list-publications).

## Add Subscription Tag

Adds tags to a subscription in Beehiiv.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/add-subscription-tag" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "publicationId": "string",
  "subscriptionId": "string",
  "tags[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/beehiiv/latest/actions/add-subscription-tag', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "publicationId": "string",
    "subscriptionId": "string",
    "tags[]": ["string"]
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

See the full [Add Subscription Tag action reference](actions/add-subscription-tag.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/beehiiv/latest/actions/add-subscription-tag).
