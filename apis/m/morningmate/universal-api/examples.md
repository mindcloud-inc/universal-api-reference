# Morningmate Universal API Examples

These examples use the MindCloud API key and Morningmate connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Search Employees

Retrieves employees from Morningmate.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-employees?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/search-employees?${params}`, {
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
      "cellPhoneNumber": "string",
      "companyPhoneNumber": "string",
      "divisionCode": "string",
      "divisionId": "string",
      "divisionName": "Ava Chen",
      "email": "ava@example.com",
      "fullname": "Ava Chen",
      "inttId": "string",
      "responsibility": "string",
      "userId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Search Employees action reference](actions/search-employees.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/morningmate/latest/actions/search-employees).

## Create Post

Creates a post in a Morningmate project.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "projectId": 1,
  "registerId": "string",
  "title": "string",
  "contents": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/morningmate/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "projectId": 1,
    "registerId": "string",
    "title": "string",
    "contents": "string"
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
      "postId": "string",
      "projectId": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Post action reference](actions/create-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/morningmate/latest/actions/create-post).
