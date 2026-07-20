# Porsline: Update Question



```
PUT https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-question" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "surveyId": 1,
  "questionId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/porsline/latest/actions/update-question', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "surveyId": 1,
    "questionId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyId` | number | yes | The id of the target survey. |
| `questionId` | number | yes | Question ID. |
| `title` | string | no | Question title. |
| `type` | number | no | Question type. |
| `steps` | number | no | Number of rating steps. |
| `iconType` | number | no | Icon type for rating questions. |
| `answerRequired` | boolean | no | Whether answering the question is required. |
| `duplicate` | string | no | Whether to duplicate the question during update. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "answer_required": true,
      "description_text": "string",
      "description_text_active": true,
      "desktop_image_layout": 1,
      "edges": [
        {}
      ],
      "html_description_text": "string",
      "html_title": "string",
      "icon_type": 1,
      "id": 1,
      "image_brightness": 1,
      "image_name": "Ava Chen",
      "image_or_video": 1,
      "image_path": "string",
      "image_position": 1,
      "image_video_active": true,
      "mobile_image_layout": 1,
      "question_number_is_hidden": true,
      "related_group": 1,
      "responding_duration": "string",
      "scores": [
        {}
      ],
      "show_charts": true,
      "steps": 1,
      "survey": 1,
      "title": "string",
      "type": 1,
      "variable_edges": [
        {}
      ],
      "video_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `answer_required` | boolean |  |
| `description_text` | string |  |
| `description_text_active` | boolean |  |
| `desktop_image_layout` | number |  |
| `edges` | array<object> |  |
| `html_description_text` | string |  |
| `html_title` | string |  |
| `icon_type` | number |  |
| `id` | number |  |
| `image_brightness` | number |  |
| `image_name` | string |  |
| `image_or_video` | number |  |
| `image_path` | string |  |
| `image_position` | number |  |
| `image_video_active` | boolean |  |
| `mobile_image_layout` | number |  |
| `question_number_is_hidden` | boolean |  |
| `related_group` | number |  |
| `responding_duration` | string |  |
| `scores` | array<object> |  |
| `show_charts` | boolean |  |
| `steps` | number |  |
| `survey` | number |  |
| `title` | string |  |
| `type` | number |  |
| `variable_edges` | array<object> |  |
| `video_url` | string |  |

## Native endpoint

Through the native Porsline API, this operation is `PATCH /api/v2/surveys/:survey_id/questions/:id/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-question.md) for the provider-specific parameters and requirements.

