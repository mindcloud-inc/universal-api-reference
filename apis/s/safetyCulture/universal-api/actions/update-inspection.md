# SafetyCulture: Update Inspection

Updates an inspection in SafetyCulture.

```
PUT https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-inspection
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SafetyCulture `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-inspection" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "auditId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/safetyCulture/latest/actions/update-inspection', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "auditId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `auditId` | string | yes | The ID of the inspection to update. |
| `archived` | boolean | no | Whether to archive or un-archive the inspection. Optional. Defaults to false (un-archive). |
| `headerItems[]` | array<object> | no | The title page items of the inspection. |
| `items[]` | array<object> | no | The items of the inspection. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "auditData": {
        "dateCompleted": "2026-05-07T12:00:00.000Z",
        "dateStarted": "2026-05-07T12:00:00.000Z",
        "name": "Ava Chen"
      },
      "auditId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `auditData.dateCompleted` | date |  |
| `auditData.dateStarted` | date |  |
| `auditData.name` | string |  |
| `auditId` | string |  |
| `createdAt` | date |  |
| `modifiedAt` | date |  |
| `templateId` | string |  |

## Native endpoint

Through the native SafetyCulture API, this operation is `PUT /audits/{audit_id}` (base URL `https://api.safetyculture.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-inspection.md) for the provider-specific parameters and requirements.

