# Candu Universal API Examples

These examples use the MindCloud API key and Candu connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Content Metadata

Retrieves content metadata records from Candu.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/candu/latest/actions/list-content-metadata?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/candu/latest/actions/list-content-metadata?${params}`, {
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
      "name": "Ava Chen",
      "slug": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Content Metadata action reference](actions/list-content-metadata.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/candu/latest/actions/list-content-metadata).

## Associate User With Group

Associates a user with a group in Candu.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/candu/latest/actions/associate-user-with-group" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "groupId": "string",
  "userId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/candu/latest/actions/associate-user-with-group', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "groupId": "string",
    "userId": "string"
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
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Associate User With Group action reference](actions/associate-user-with-group.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/candu/latest/actions/associate-user-with-group).
