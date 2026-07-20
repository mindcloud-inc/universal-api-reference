# EducateMe: List Course Activities

Lists course activities in EducateMe.

```
GET https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-course-activities
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EducateMe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-course-activities?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/educateMe/latest/actions/list-course-activities?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes |  |
| `activityId` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "activityLink": "https://example.com",
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
| `activityLink` | string |  |
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

Through the native EducateMe API, this operation is `GET /courses/:id/lessons` (base URL `https://api.educate-me.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-course-activities.md) for the provider-specific parameters and requirements.

