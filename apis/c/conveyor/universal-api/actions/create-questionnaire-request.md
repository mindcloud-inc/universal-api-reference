# Conveyor: Create Questionnaire Request

Creates a questionnaire request in Conveyor.

```
POST https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-questionnaire-request
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-questionnaire-request" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-questionnaire-request', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `externalId` | string | no | External questionnaire request identifier. |
| `source` | string | no | Source system for the request. |
| `submitterEmail` | string | no | Submitter email address. |
| `submitterExternalId` | string | no | External submitter identifier. |
| `submitterExternalName` | string | no | External submitter name. |
| `caseIds` | string<string> | no | Salesforce case identifiers for questionnaire import. |
| `rawData` | string | no | Raw questionnaire request data. |
| `file` | file | no | Questionnaire request file upload. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_embedded": {
        "questionnaire_requests": [
          {
            "external_id": "string",
            "id": "string",
            "source": "string",
            "status": "string",
            "submitter_email": "ava@example.com",
            "submitter_external_id": "string",
            "submitter_external_name": "Ava Chen"
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_embedded` | object |  |
| `_embedded.questionnaire_requests` | array<object> |  |
| `_embedded.questionnaire_requests[].external_id` | string |  |
| `_embedded.questionnaire_requests[].id` | string |  |
| `_embedded.questionnaire_requests[].source` | string |  |
| `_embedded.questionnaire_requests[].status` | string |  |
| `_embedded.questionnaire_requests[].submitter_email` | string |  |
| `_embedded.questionnaire_requests[].submitter_external_id` | string |  |
| `_embedded.questionnaire_requests[].submitter_external_name` | string |  |

## Native endpoint

Through the native Conveyor API, this operation is `POST /v2/questionnaire_requests` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-questionnaire-request.md) for the provider-specific parameters and requirements.

