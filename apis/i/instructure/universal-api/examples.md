# Instructure Universal API Examples

These examples use the MindCloud API key and Instructure connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Instructure Canvas.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-current-user?${params}`, {
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
      "avatarUrl": "https://example.com",
      "createdAt": "string",
      "effectiveLocale": "string",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen",
      "locale": "string",
      "name": "Ava Chen",
      "permissions": {},
      "shortName": "Ava Chen",
      "sortableName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instructure/latest/actions/get-current-user).

## Add Course To Favorites

Adds a course to favorites in Instructure Canvas.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/add-course-to-favorites" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/add-course-to-favorites', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
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
      "context_id": 1,
      "context_type": "string",
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Course To Favorites action reference](actions/add-course-to-favorites.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/instructure/latest/actions/add-course-to-favorites).
