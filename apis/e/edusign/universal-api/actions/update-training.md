# Edusign: Update Training

Updates an existing training in Edusign.

```
PUT https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-training
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-training" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trainingId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/update-training', {
  method: 'PUT',
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
| `trainingId` | string | yes | Training ID |
| `name` | string | no | Training name |
| `start` | string | no | Start date of the training (format YYYY-MM-DD, ISO 8601) |
| `end` | string | no | End date of the training (format YYYY-MM-DD, ISO 8601) |
| `goals` | string | no | Training goals |
| `apiId` | string | no | The ID of your API resource representing the training |
| `apiType` | string | no | The name of your API from where you created the training |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `tags[]` | array<string> | no |  |
| `registrationOptions` | object | no |  |
| `registrationOptions.pastSheets` | boolean | no | If you want to add the students to past attendance sheets |
| `registrationOptions.pastDocuments` | boolean | no | If you want to add the students to past documents |
| `registrationOptions.pastSurveys` | boolean | no | If you want to add the students to past surveys |
| `registrationOptions.futureSheets` | boolean | no | If you want to add the students to future attendance sheets |
| `registrationOptions.futureDocuments` | boolean | no | If you want to add the students to future documents |
| `registrationOptions.futureSurveys` | boolean | no | If you want to add the students to future surveys |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": true,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | boolean |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `PUT /v1/trainings/:trainingId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-training.md) for the provider-specific parameters and requirements.

