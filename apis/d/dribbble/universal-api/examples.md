# Dribbble Universal API Examples

These examples use the MindCloud API key and Dribbble connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Current User



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/get-current-user?${params}`, {
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
      "bio": "string",
      "canUploadShot": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "followersCount": 1,
      "htmlUrl": "https://example.com",
      "id": 1,
      "links": {},
      "location": "string",
      "login": "string",
      "name": "Ava Chen",
      "pro": true,
      "teams": [
        {}
      ],
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Current User action reference](actions/get-current-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dribbble/latest/actions/get-current-user).

## Create Job



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/create-job" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "organizationName": "Ava Chen",
  "title": "string",
  "location": "string",
  "linkToApply": "https://example.com",
  "description": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dribbble/latest/actions/create-job', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "organizationName": "Ava Chen",
    "title": "string",
    "location": "string",
    "linkToApply": "https://example.com",
    "description": "string"
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
      "category": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "endsAt": "2026-05-07T12:00:00.000Z",
      "facebook": "string",
      "id": 1,
      "instagram": "string",
      "linkToApply": "https://example.com",
      "location": "string",
      "organizationName": "Ava Chen",
      "roleType": "string",
      "startsAt": "2026-05-07T12:00:00.000Z",
      "team": {},
      "title": "string",
      "twitter": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com",
      "website": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Job action reference](actions/create-job.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dribbble/latest/actions/create-job).
