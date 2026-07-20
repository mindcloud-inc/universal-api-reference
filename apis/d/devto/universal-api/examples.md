# Dev.to Universal API Examples

These examples use the MindCloud API key and Dev.to connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated Dev.to user.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-authenticated-user?${params}`, {
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
      "id": 1,
      "location": "string",
      "name": "Ava Chen",
      "profile_image": "string",
      "summary": "string",
      "username": "Ava Chen",
      "website_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/devto/latest/actions/get-authenticated-user).

## Create Reaction

Creates a reaction to an article, comment, or user in Dev.to.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/devto/latest/actions/create-reaction" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "category": "0",
  "reactableId": 1,
  "reactableType": "0"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/devto/latest/actions/create-reaction', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "category": "0",
    "reactableId": 1,
    "reactableType": "0"
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
      "category": "string",
      "id": 1,
      "reactable_id": 1,
      "reactable_type": "string",
      "result": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Reaction action reference](actions/create-reaction.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/devto/latest/actions/create-reaction).
