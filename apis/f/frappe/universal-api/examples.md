# Frappe Universal API Examples

These examples use the MindCloud API key and Frappe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Logged User

Retrieves the logged-in user from Frappe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-logged-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/frappe/latest/actions/get-logged-user?${params}`, {
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
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Logged User action reference](actions/get-logged-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/frappe/latest/actions/get-logged-user).

## Add Comment To Document V2

Adds a comment to a Frappe document.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/frappe/latest/actions/add-comment-to-document-v2" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/frappe/latest/actions/add-comment-to-document-v2', {
  method: 'PUT',
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
      "data": {}
    }
  ],
  "meta": {}
}
```

See the full [Add Comment To Document V2 action reference](actions/add-comment-to-document-v2.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/frappe/latest/actions/add-comment-to-document-v2).
