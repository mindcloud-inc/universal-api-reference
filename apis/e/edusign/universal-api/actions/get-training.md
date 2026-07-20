# Edusign: Get Training

Retrieves a training from Edusign by ID.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-training
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-training?connectionId=$CONNECTION_ID&trainingId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trainingId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-training?${params}`, {
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
| `trainingId` | string | yes | Training ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "apiId": "string",
        "apiType": "string",
        "archived": 1,
        "creatorId": "string",
        "dateCreated": "string",
        "dateUpdated": "string",
        "end": "string",
        "goals": "string",
        "hasUncompleteDocuments": true,
        "id": "string",
        "name": "Ava Chen",
        "professorIds": [
          "string"
        ],
        "registrationOptions": {
          "futureDocuments": true,
          "futureSheets": true,
          "futureSurveys": true,
          "pastDocuments": true,
          "pastSheets": true,
          "pastSurveys": true
        },
        "schoolId": "string",
        "start": "string",
        "studentIds": [
          "string"
        ],
        "studentInscriptionHash": "string",
        "tags": [
          "string"
        ]
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
| `result.apiId` | string |  |
| `result.apiType` | string |  |
| `result.archived` | number |  |
| `result.creatorId` | string |  |
| `result.dateCreated` | string |  |
| `result.dateUpdated` | string |  |
| `result.end` | string |  |
| `result.goals` | string |  |
| `result.hasUncompleteDocuments` | boolean |  |
| `result.id` | string |  |
| `result.name` | string |  |
| `result.professorIds` | array<string> |  |
| `result.registrationOptions` | object |  |
| `result.registrationOptions.futureDocuments` | boolean |  |
| `result.registrationOptions.futureSheets` | boolean |  |
| `result.registrationOptions.futureSurveys` | boolean |  |
| `result.registrationOptions.pastDocuments` | boolean |  |
| `result.registrationOptions.pastSheets` | boolean |  |
| `result.registrationOptions.pastSurveys` | boolean |  |
| `result.schoolId` | string |  |
| `result.start` | string |  |
| `result.studentIds` | array<string> |  |
| `result.studentInscriptionHash` | string |  |
| `result.tags` | array<string> |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v1/trainings/:trainingId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-training.md) for the provider-specific parameters and requirements.

