# Basecamp Universal API Examples

These examples use the MindCloud API key and Basecamp connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authorization

Retrieves authorization details and accessible accounts from Basecamp.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-authorization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/get-authorization?${params}`, {
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

See the full [Get Authorization action reference](actions/get-authorization.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/basecamp/latest/actions/get-authorization).

## Complete Todo

Marks a to-do as completed in Basecamp.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/complete-todo" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "accountId": "6172410",
  "todoId": "9660797208"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/basecamp/latest/actions/complete-todo', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "accountId": "6172410",
    "todoId": "9660797208"
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

See the full [Complete Todo action reference](actions/complete-todo.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/basecamp/latest/actions/complete-todo).
