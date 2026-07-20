# PickFu: Update Survey



```
PUT https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/update-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PickFu `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/update-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pickFu/latest/actions/update-survey', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Survey GUID. |
| `name` | string | no | Survey name. |
| `projectId` | string | no | Project GUID or numeric ID, or null to remove the project. |
| `questions[]` | array<object> | no | Questions to replace all existing questions. |
| `tags[]` | array<object> | no | Tags to replace all existing tags. |
| `targeting[]` | array<string> | no | Targeting trait permalinks. |
| `reporting[]` | array<string> | no | Reporting trait permalinks. |
| `country` | string | no | Two-letter country code. |
| `sampleSize` | string | no | Number of respondents. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `surveyIntent` | string | no | Original intent of the survey as interpreted by AI. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "country": "string",
      "id": "string",
      "name": "Ava Chen",
      "numResponses": 1,
      "questions": [
        {}
      ],
      "reporting": [
        "string"
      ],
      "sampleSize": 1,
      "status": "string",
      "surveyUrl": "https://example.com",
      "targeting": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `id` | string |  |
| `name` | string |  |
| `numResponses` | number |  |
| `questions` | array<object> |  |
| `reporting` | array<string> |  |
| `sampleSize` | number |  |
| `status` | string |  |
| `surveyUrl` | string |  |
| `targeting` | array<string> |  |

## Native endpoint

Through the native PickFu API, this operation is `PATCH /surveys/[:id]` (base URL `https://api.pickfu.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-survey.md) for the provider-specific parameters and requirements.

