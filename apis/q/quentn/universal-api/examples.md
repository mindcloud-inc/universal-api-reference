# Quentn Universal API Examples

These examples use the MindCloud API key and Quentn connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contact Comments



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-comments?connectionId=$CONNECTION_ID&contactId=123" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "contactId": "123"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/quentn/latest/actions/list-contact-comments?${params}`, {
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
      "comments": [
        {}
      ],
      "limit": 1,
      "numberComments": "string",
      "numberRanges": 1,
      "range": 1,
      "sort": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contact Comments action reference](actions/list-contact-comments.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quentn/latest/actions/list-contact-comments).

## Add Contact Comment



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/quentn/latest/actions/add-contact-comment" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "123",
  "comment": "Reached out after webinar signup"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/quentn/latest/actions/add-contact-comment', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "123",
    "comment": "Reached out after webinar signup"
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
      "commentId": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Add Contact Comment action reference](actions/add-contact-comment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/quentn/latest/actions/add-contact-comment).
