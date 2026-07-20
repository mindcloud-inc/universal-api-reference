# PostHog Universal API Examples

These examples use the MindCloud API key and PostHog connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Organizations

Retrieves organizations from PostHog.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postHog/latest/actions/list-organizations?${params}`, {
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
      "created_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "member_count": 1,
      "membership_level": 1,
      "name": "Ava Chen",
      "slug": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Organizations action reference](actions/list-organizations.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postHog/latest/actions/list-organizations).

## Add or Invite Members

Creates an organization invite in PostHog.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postHog/latest/actions/add-or-invite-members" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationId": "0196354e-4380-0000-cc07-8aa6be2ca63f",
  "targetEmail": "teammate@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postHog/latest/actions/add-or-invite-members', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationId": "0196354e-4380-0000-cc07-8aa6be2ca63f",
    "targetEmail": "teammate@example.com"
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
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": {},
      "emailingAttemptMade": true,
      "firstName": "Ava",
      "id": "string",
      "isExpired": true,
      "level": 1,
      "message": "string",
      "privateProjectAccess": [
        {}
      ],
      "targetEmail": "ava@example.com",
      "updatedAt": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add or Invite Members action reference](actions/add-or-invite-members.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/postHog/latest/actions/add-or-invite-members).
