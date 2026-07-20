# EducateMe: Create Activity

Creates a new activity in EducateMe.

```
POST https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/create-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

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

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityDetails.title` | string | yes |  |
| `activityDetails.mainHtml` | string | yes |  |
| `activityDetails.isDraft` | boolean | yes |  |
| `activityDetails.feedbackRequired` | boolean | yes |  |
| `activityDetails.type` | string | yes |  |
| `courseId` | string | yes |  |
| `moduleId` | string | yes |  |

## Response

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

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `activityLink` | string |  |
| `aiAssessment` | object |  |
| `certification` | object |  |
| `feedbackRequired` | boolean |  |
| `homeAssignment.id` | string |  |
| `id` | string |  |
| `isDraft` | boolean |  |
| `mainHtml` | string |  |
| `module` | object |  |
| `order` | number |  |
| `peerReview` | object |  |
| `quiz` | object |  |
| `title` | string |  |
| `type` | string |  |

## Native endpoint

Through the native EducateMe API, this operation is `POST /activities` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-activity.md) for the provider-specific parameters and requirements.

