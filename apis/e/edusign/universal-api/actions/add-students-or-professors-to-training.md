# Edusign: Add Students Or Professors To Training

Adds students or professors to a training in Edusign.

```
POST https://connect.mindcloud.co/v1/universal/edusign/latest/actions/add-students-or-professors-to-training
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/add-students-or-professors-to-training" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trainingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/add-students-or-professors-to-training', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trainingId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trainingId` | string | yes | The unique ID of the training |
| `studentsIds[]` | array<string> | no |  |
| `professorsIds[]` | array<string> | no |  |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `options` | object | no |  |
| `options.pastSheets` | boolean | no | If you want to add the students to past attendance sheets |
| `options.pastDocuments` | boolean | no | If you want to add the students to past documents |
| `options.pastSurveys` | boolean | no | If you want to add the students to past surveys |
| `options.futureSheets` | boolean | no | If you want to add the students to future attendance sheets |
| `options.futureDocuments` | boolean | no | If you want to add the students to future documents |
| `options.futureSurveys` | boolean | no | If you want to add the students to future surveys |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v1/trainings/resources/:trainingId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-students-or-professors-to-training.md) for the provider-specific parameters and requirements.

