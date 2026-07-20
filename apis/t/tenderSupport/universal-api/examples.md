# Tender Support Universal API Examples

These examples use the MindCloud API key and Tender Support connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Site

Retrieves site details from Tender Support.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-site?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/get-site?${params}`, {
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
      "categoriesHref": "string",
      "discussionsHref": "string",
      "faqsHref": "string",
      "href": "string",
      "htmlHref": "string",
      "name": "Ava Chen",
      "permalink": "https://example.com",
      "profileHref": "string",
      "sectionsHref": "string",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Site action reference](actions/get-site.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tenderSupport/latest/actions/get-site).

## Create User

Creates a new user in Tender Support.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/create-user" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "email": "ava@example.com",
  "password": "string",
  "passwordConfirmation": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/tenderSupport/latest/actions/create-user', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "email": "ava@example.com",
    "password": "string",
    "passwordConfirmation": "string"
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
      "activatedAt": "2026-05-07T12:00:00.000Z",
      "commentsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "discussionsCount": 1,
      "discussionsHref": "string",
      "email": "ava@example.com",
      "enableEmailNotifications": true,
      "externalId": "string",
      "href": "string",
      "name": "Ava Chen",
      "openidUrl": "https://example.com",
      "publicFacing": true,
      "state": "string",
      "title": "string",
      "trusted": true,
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Create User action reference](actions/create-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/tenderSupport/latest/actions/create-user).
