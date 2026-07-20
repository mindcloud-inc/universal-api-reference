# SurveySparrow: Update Survey Folder

Updates an existing survey folder in SurveySparrow.

```
PUT https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-survey-folder
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-survey-folder" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/update-survey-folder', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | number | yes | ID of the survey folder |
| `name` | string | no | Name of the survey folder |
| `visibility` | list | no | Visibility of the survey folder |
| `teams[]` | array<number> | no | Teams with access |
| `users[]` | array<number> | no | Users with access |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "auto_created": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "created_by": 1,
      "deleted_at": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": 1,
      "name": "Ava Chen",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "visibility": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `account_id` | number |  |
| `auto_created` | boolean |  |
| `created_at` | date |  |
| `created_by` | number |  |
| `deleted_at` | date |  |
| `description` | string |  |
| `id` | number |  |
| `name` | string |  |
| `updated_at` | date |  |
| `visibility` | string |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `PATCH /survey_folders/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-survey-folder.md) for the provider-specific parameters and requirements.

