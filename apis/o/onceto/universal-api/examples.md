# Once.to Universal API Examples

These examples use the MindCloud API key and Once.to connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User

Retrieves the current user from Once.to.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onceto/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onceto/latest/actions/get-current-user?${params}`, {
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
      "id": "string",
      "isTeam": true,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onceto/latest/actions/get-current-user).

## Create Short Link

Creates a new short link in Once.to.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onceto/latest/actions/create-short-link" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com/offer"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onceto/latest/actions/create-short-link', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com/offer"
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
      "active": true,
      "banned": true,
      "banTime": "2026-05-07T12:00:00.000Z",
      "botClicks": true,
      "clickCount": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "customSlug": true,
      "expires": "2026-05-07T12:00:00.000Z",
      "failedCount": 1,
      "id": "string",
      "lastClicked": "2026-05-07T12:00:00.000Z",
      "ownerId": "string",
      "rules": {},
      "shortUrl": "https://example.com",
      "slug": "string",
      "starts": "2026-05-07T12:00:00.000Z",
      "statusCode": 1,
      "tags": [
        "string"
      ],
      "targetUrl": "https://example.com",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Short Link action reference](actions/create-short-link.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onceto/latest/actions/create-short-link).
