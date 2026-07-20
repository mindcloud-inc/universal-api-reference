# Zoho CRM: Upsert Lead

Finds a lead in Zoho CRM, or creates one if needed.

```
POST https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/upsert-lead
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/upsert-lead" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ],
  "data[].lastName": "Wizard Lead 20260311 2"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCRM/latest/actions/upsert-lead', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}],
    "data[].lastName": "Wizard Lead 20260311 2"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data[]` | array<object> | yes | Lead records to upsert. |
| `data[].lastName` | string | yes | Example: `Wizard Lead 20260311 2`. |
| `data[].company` | string | no | Example: `MindCloud Wizard Upsert`. |
| `data[].email` | string | no | Example: `wizard.lead.20260311.2@example.com`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "action": "string",
      "code": "string",
      "details": {
        "createdBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "createdTime": "2026-05-07T12:00:00.000Z",
        "id": "string",
        "modifiedBy": {
          "id": "string",
          "name": "Ava Chen"
        },
        "modifiedTime": "2026-05-07T12:00:00.000Z"
      },
      "duplicateField": "string",
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `action` | string |  |
| `code` | string |  |
| `details.createdBy.id` | string |  |
| `details.createdBy.name` | string |  |
| `details.createdTime` | date |  |
| `details.id` | string |  |
| `details.modifiedBy.id` | string |  |
| `details.modifiedBy.name` | string |  |
| `details.modifiedTime` | date |  |
| `duplicateField` | string |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho CRM API, this operation is `POST /Leads/upsert` (base URL `{{credentials.accessTokenRequest.api_domain}}/crm/v8`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upsert-lead.md) for the provider-specific parameters and requirements.

