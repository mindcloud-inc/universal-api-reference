# Box Universal API Examples

These examples use the MindCloud API key and Box connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/box/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/box/latest/actions/get-current-user?${params}`, {
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
      "avatar_url": "https://example.com",
      "created_at": "2026-05-07T12:00:00.000Z",
      "enterprise": {},
      "external_app_user_id": "string",
      "hostname": "Ava Chen",
      "id": "string",
      "is_platform_access_only": true,
      "language": "string",
      "login": "string",
      "max_upload_size": 1,
      "modified_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "role": "string",
      "space_amount": 1,
      "space_used": 1,
      "status": "string",
      "timezone": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/box/latest/actions/get-current-user).

## Commit Upload Session



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/box/latest/actions/commit-upload-session" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sessionId": "578EAA0B34295198B0E32B085769932C",
  "wholeFileSha1": "SGVsbG8gQm94",
  "parts": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/box/latest/actions/commit-upload-session', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sessionId": "578EAA0B34295198B0E32B085769932C",
    "wholeFileSha1": "SGVsbG8gQm94",
    "parts": [{}]
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
      "contentCreatedAt": "string",
      "contentModifiedAt": "string",
      "createdAt": "string",
      "createdBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "description": "string",
      "etag": "string",
      "fileVersion": {
        "id": "string",
        "sha1": "string",
        "type": "string"
      },
      "id": "string",
      "itemStatus": "string",
      "modifiedAt": "string",
      "modifiedBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "name": "Ava Chen",
      "ownedBy": {
        "id": "string",
        "login": "string",
        "name": "Ava Chen",
        "type": "string"
      },
      "parent": {
        "etag": {},
        "id": "string",
        "name": "Ava Chen",
        "sequenceId": {},
        "type": "string"
      },
      "pathCollection": {
        "entries": [
          {
            "etag": {},
            "id": "string",
            "name": "Ava Chen",
            "sequenceId": {},
            "type": "string"
          }
        ],
        "totalCount": 1
      },
      "purgedAt": {},
      "sequenceId": "string",
      "sha1": "string",
      "sharedLink": {},
      "size": 1,
      "trashedAt": {},
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Commit Upload Session action reference](actions/commit-upload-session.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/box/latest/actions/commit-upload-session).
