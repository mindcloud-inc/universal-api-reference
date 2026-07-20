# GitBook Universal API Examples

These examples use the MindCloud API key and GitBook connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Authenticated User

Retrieves the authenticated user from GitBook.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/get-authenticated-user?${params}`, {
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
      "displayName": "Ava Chen",
      "email": "ava@example.com",
      "id": "string",
      "photoURL": "https://example.com",
      "urls": {
        "location": "https://example.com"
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Authenticated User action reference](actions/get-authenticated-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gitBook/latest/actions/get-authenticated-user).

## Add Space To Site

Adds an existing space to a GitBook site.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/add-space-to-site" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "string",
  "siteId": "string",
  "spaceId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gitBook/latest/actions/add-space-to-site', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "string",
    "siteId": "string",
    "spaceId": "string"
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
      "default": true,
      "draft": true,
      "hasAdvancedCustomizationFeature": true,
      "hidden": true,
      "id": "string",
      "object": "string",
      "path": "string",
      "space": {
        "createdAt": "2026-05-07T12:00:00.000Z",
        "defaultLevel": "string",
        "editMode": "string",
        "emoji": "string",
        "id": "string",
        "organization": "string",
        "revision": "string",
        "title": "string",
        "updatedAt": "2026-05-07T12:00:00.000Z",
        "urls": {
          "app": "https://example.com",
          "location": "https://example.com"
        },
        "visibility": "string"
      },
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add Space To Site action reference](actions/add-space-to-site.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gitBook/latest/actions/add-space-to-site).
