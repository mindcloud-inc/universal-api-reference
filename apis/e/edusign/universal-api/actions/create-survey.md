# Edusign: Create Survey

Creates a new survey in Edusign.

```
POST https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-survey
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-survey" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "survey": "string",
  "students[]": [
    "string"
  ],
  "professors[]": [
    "string"
  ],
  "externals[]": [
    "string"
  ],
  "sendingDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-survey', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "survey": "string",
    "students[]": ["string"],
    "professors[]": ["string"],
    "externals[]": ["string"],
    "sendingDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `survey` | string | yes | Template ID of the survey |
| `students[]` | array<string> | yes |  |
| `professors[]` | array<string> | yes |  |
| `externals[]` | array<string> | yes |  |
| `sendingDate` | string | yes | Sending date |
| `trainingId` | string | no | Training ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "id": "string"
      },
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | object |  |
| `result.id` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v1/surveys` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-survey.md) for the provider-specific parameters and requirements.

