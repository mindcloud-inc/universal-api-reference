# Conveyor: Create Questionnaire

Creates a questionnaire record in Conveyor.

```
POST https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-questionnaire
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Conveyor `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-questionnaire" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "domain": "string",
  "email": "ava@example.com",
  "originalFormat": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/conveyor/latest/actions/create-questionnaire', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "domain": "string",
    "email": "ava@example.com",
    "originalFormat": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `contentType` | string | no | Uploaded questionnaire content type. |
| `contentVersionId` | string | no | Salesforce content version identifier. |
| `crmId` | string | no | CRM identifier associated with the questionnaire. |
| `customerName` | string | no | Customer name associated with the questionnaire. |
| `domain` | string | yes | Company domain for the questionnaire. |
| `filename` | string | no | Uploaded questionnaire filename. |
| `notes` | string | no | Additional questionnaire notes. |
| `portalUrl` | string | no | Portal URL for portal-based questionnaires. |
| `questionnaireType` | string | no | Questionnaire type. |
| `email` | string | yes | Recipient or customer email for the questionnaire. |
| `originalFormat` | string | yes | Original questionnaire format. |
| `dueAt` | date | no | Questionnaire due date. |
| `productLineIds` | string<string> | no | Product line identifiers to associate with the questionnaire. |
| `file` | file | no | Questionnaire file upload. |
| `crmAmount` | number | no | CRM deal amount associated with the questionnaire. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "_type": "string",
      "created_at": "2026-05-07T12:00:00.000Z",
      "due_at": "2026-05-07T12:00:00.000Z",
      "id": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_type` | string |  |
| `created_at` | date |  |
| `due_at` | date |  |
| `id` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Conveyor API, this operation is `POST /v2/questionnaires` (base URL `https://api.conveyor.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-questionnaire.md) for the provider-specific parameters and requirements.

