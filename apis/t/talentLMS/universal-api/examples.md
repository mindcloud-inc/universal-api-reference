# TalentLMS Universal API Examples

These examples use the MindCloud API key and TalentLMS connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from a TalentLMS domain.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/list-users?${params}`, {
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
      "avatar": {},
      "email": "ava@example.com",
      "id": 1,
      "lastLogin": "string",
      "lastUpdated": "string",
      "login": "string",
      "name": "Ava Chen",
      "registration": "string",
      "status": "string",
      "surname": "Ava Chen",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/talentLMS/latest/actions/list-users).

## Add Course to Branch

Adds a course to a branch in TalentLMS.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/add-course-to-branch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "branchId": 1,
  "courseId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/talentLMS/latest/actions/add-course-to-branch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "branchId": 1,
    "courseId": 1
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

See the full [Add Course to Branch action reference](actions/add-course-to-branch.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/talentLMS/latest/actions/add-course-to-branch).
