# SurveySparrow: Get Survey Folder

Retrieves a survey folder from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-survey-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-survey-folder?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-survey-folder?${params}`, {
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
| `id` | number | yes | ID of the survey folder |

## Response

```json
{
  "success": true,
  "data": [
    {
      "auto_created": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `auto_created` | boolean |  |
| `created_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `visibility` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /survey_folders/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-survey-folder.md) for the provider-specific parameters and requirements.

