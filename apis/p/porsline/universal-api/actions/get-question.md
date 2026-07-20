# Porsline: Get Question



```
GET https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-question
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Porsline `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-question?connectionId=$CONNECTION_ID&surveyId=213151&questionId=3375762" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "surveyId": "213151",
  "questionId": "3375762"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/porsline/latest/actions/get-question?${params}`, {
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
| `surveyId` | number | yes | The id of the target survey. Example: `213151`. |
| `questionId` | number | yes | Question ID. Example: `3375762`. |

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

Through the native Porsline API, this operation is `GET /api/v2/surveys/:survey_id/questions/:id/` (base URL `https://survey.porsline.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-question.md) for the provider-specific parameters and requirements.

