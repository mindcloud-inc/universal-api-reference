# StoryChief Universal API Examples

These examples use the MindCloud API key and StoryChief connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from StoryChief.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/get-current-user?${params}`, {
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
      "account": {
        "data": {
          "id": 1,
          "name": "Ava Chen"
        }
      },
      "email": "ava@example.com",
      "firstname": "Ava",
      "id": 1,
      "lastname": "Chen",
      "phone": "string",
      "profilePicture": {
        "data": {
          "alt": "string",
          "name": "Ava Chen",
          "sizes": {
            "full": "string",
            "large": "string",
            "regular": "string"
          },
          "url": "https://example.com"
        }
      },
      "role": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storyChief/latest/actions/get-current-user).

## Create Author

Creates a new author in StoryChief.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/create-author" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/storyChief/latest/actions/create-author', {
  method: 'POST',
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
  "data": [],
  "meta": {}
}
```

See the full [Create Author action reference](actions/create-author.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/storyChief/latest/actions/create-author).
