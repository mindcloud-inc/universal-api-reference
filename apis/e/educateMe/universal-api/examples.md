# EducateMe Universal API Examples

These examples use the MindCloud API key and EducateMe connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Lists users in EducateMe.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-users?${params}`, {
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
      "name": "Ava Chen",
      "roles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/educateMe/latest/actions/list-users).

## Create Activity

Creates a new activity in EducateMe.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityDetails.title": "string",
  "activityDetails.mainHtml": "string",
  "activityDetails.isDraft": true,
  "activityDetails.feedbackRequired": true,
  "activityDetails.type": "string",
  "courseId": "string",
  "moduleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-activity', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityDetails.title": "string",
    "activityDetails.mainHtml": "string",
    "activityDetails.isDraft": true,
    "activityDetails.feedbackRequired": true,
    "activityDetails.type": "string",
    "courseId": "string",
    "moduleId": "string"
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
      "activityLink": "https://example.com",
      "aiAssessment": {},
      "certification": {},
      "feedbackRequired": true,
      "homeAssignment": {
        "id": "string"
      },
      "id": "string",
      "isDraft": true,
      "mainHtml": "string",
      "module": {},
      "order": 1,
      "peerReview": {},
      "quiz": {},
      "title": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Activity action reference](actions/create-activity.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/educateMe/latest/actions/create-activity).
