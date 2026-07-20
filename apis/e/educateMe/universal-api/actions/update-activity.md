# EducateMe: Update Activity

Updates an existing activity in EducateMe.

```
PUT https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-activity
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-activity" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "activityId": "string",
  "title": "string",
  "mainHtml": "string",
  "isDraft": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/update-activity', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "activityId": "string",
    "title": "string",
    "mainHtml": "string",
    "isDraft": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `activityId` | string | yes |  |
| `title` | string | yes |  |
| `mainHtml` | string | yes |  |
| `isDraft` | boolean | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "aiAssessment": {},
      "certification": {},
      "feedbackRequired": true,
      "homeAssignment": {},
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
| `aiAssessment` | object |  |
| `certification` | object |  |
| `feedbackRequired` | boolean |  |
| `homeAssignment` | object |  |
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

Through the native EducateMe API, this operation is `POST /activities/:activityId/update` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-activity.md) for the provider-specific parameters and requirements.

