# Sentry IO Universal API Examples

These examples use the MindCloud API key and Sentry IO connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Your Organizations

Retrieves your organizations from Sentry IO.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-your-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/list-your-organizations?${params}`, {
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
      "dateCreated": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "links": {},
      "name": "Ava Chen",
      "slug": "string",
      "status": {}
    }
  ],
  "meta": {}
}
```

See the full [List Your Organizations action reference](actions/list-your-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sentryIO/latest/actions/list-your-organizations).

## Update Issue

Updates an existing issue in Sentry IO.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/update-issue" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationIdOrSlug": "my-org",
  "issueId": "123456789"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sentryIO/latest/actions/update-issue', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationIdOrSlug": "my-org",
    "issueId": "123456789"
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
      "assignedTo": {},
      "id": "string",
      "isBookmarked": true,
      "isSubscribed": true,
      "shortId": "string",
      "status": "string",
      "title": "string"
    }
  ],
  "meta": {}
}
```

See the full [Update Issue action reference](actions/update-issue.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sentryIO/latest/actions/update-issue).
