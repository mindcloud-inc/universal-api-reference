# Weekdone Universal API Examples

These examples use the MindCloud API key and Weekdone connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Company Info

Retrieves company details from Weekdone.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/get-company-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/get-company-info?${params}`, {
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Company Info action reference](actions/get-company-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weekdone/latest/actions/get-company-info).

## Add Item Comment

Creates a comment on an item in Weekdone.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/add-item-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "comment": "string",
  "itemId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/weekdone/latest/actions/add-item-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "comment": "string",
    "itemId": 1
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
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Item Comment action reference](actions/add-item-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/weekdone/latest/actions/add-item-comment).
