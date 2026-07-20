# SurveySparrow: List Surveys

Retrieves all surveys from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-surveys
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-surveys?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/list-surveys?${params}`, {
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
| `surveyType` | list | no | Filter surveys by survey type. One of: `0`, `1`, `10`, `2`, `3`, `4`, `5`, `6`, `7`, `8`, `9`. |
| `archived` | boolean | no | Include archived or active surveys. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyFolderId` | string | no | Filter surveys by the containing survey folder. |
| `createdDateGte` | date | no | Return surveys created on or after this date. |
| `createdDateLte` | date | no | Return surveys created on or before this date. |
| `updatedDateGte` | date | no | Return surveys updated on or after this date. |
| `updatedDateLte` | date | no | Return surveys updated on or before this date. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "created_at": {},
      "id": 1,
      "name": "Ava Chen",
      "question_count": 1,
      "response_count": 1,
      "survey_folder_id": 1,
      "survey_folder_name": "Ava Chen",
      "survey_theme_properties": {},
      "survey_type": "string",
      "theme_id": 1,
      "updated_at": {},
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `created_at` | object |  |
| `id` | number |  |
| `name` | string |  |
| `question_count` | number |  |
| `response_count` | number |  |
| `survey_folder_id` | number |  |
| `survey_folder_name` | string |  |
| `survey_theme_properties` | object |  |
| `survey_type` | string |  |
| `theme_id` | number |  |
| `updated_at` | object |  |
| `visibility` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /surveys` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-surveys.md) for the provider-specific parameters and requirements.

