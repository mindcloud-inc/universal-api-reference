# LinkedIn Universal API Examples

These examples use the MindCloud API key and LinkedIn connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User Info

Retrieves the authenticated user's profile from LinkedIn.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/get-user-info?${params}`, {
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
      "email": "ava@example.com",
      "emailVerified": true,
      "familyName": "Ava Chen",
      "givenName": "Ava Chen",
      "locale": {
        "country": "string",
        "language": "string"
      },
      "name": "Ava Chen",
      "sub": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get User Info action reference](actions/get-user-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkedin/latest/actions/get-user-info).

## Create Post

Creates a new post in LinkedIn.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/create-post" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "author": "urn:li:organization:5515715",
  "commentary": "Sample text post created from LinkedIn API"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/linkedin/latest/actions/create-post', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "author": "urn:li:organization:5515715",
    "commentary": "Sample text post created from LinkedIn API"
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
      "value": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Post action reference](actions/create-post.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/linkedin/latest/actions/create-post).
