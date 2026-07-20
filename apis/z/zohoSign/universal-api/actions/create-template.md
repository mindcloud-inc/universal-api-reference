# Zoho Sign: Create Template

Creates a template in Zoho Sign.

```
POST https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "data": {},
  "data.templates": {},
  "data.templates.template_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "data": {},
    "data.templates": {},
    "data.templates.template_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | PDF file to upload as the template source document. |
| `data` | object | yes | Zoho Sign template payload wrapper. |
| `data.templates` | object | yes | Template details. |
| `data.templates.template_name` | string | yes | Name of the template. |
| `data.templates.request_type_id` | string | no | Document category identifier for the template. |
| `data.templates.notes` | string | no | Common message sent to all recipients. |
| `data.templates.expiration_days` | number | no | Number of days before documents from this template expire. |
| `data.templates.is_sequential` | boolean | no | Whether signers must act in order. |
| `data.templates.email_reminders` | boolean | no | Whether reminder emails are enabled. |
| `data.templates.reminder_period` | number | no | Reminder frequency in days. |
| `data.templates.folder_id` | string | no | Folder identifier where the template should be stored. |
| `data.templates.actions[]` | array<object> | no | Role rows for the template. |
| `data.templates.actions[].action_type` | string | no | Role action type such as SIGN. |
| `data.templates.actions[].role` | string | no | Template role name such as Signer. |
| `data.templates.actions[].recipient_name` | string | no | Recipient full name for the role. |
| `data.templates.actions[].recipient_email` | string | no | Recipient email address for the role. |
| `data.templates.actions[].signing_order` | number | no | Sequential order number for the role. |
| `data.templates.actions[].verify_recipient` | boolean | no | Whether recipients in this role must be verified. |
| `data.templates.actions[].verification_type` | string | no | Verification method such as EMAIL. |
| `data.templates.actions[].verification_code` | string | no | Verification code when required. |
| `data.templates.actions[].private_notes` | string | no | Private instructions for this role. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.templates.actions[].in_person_name` | string | no | Host name for in-person signing roles. |
| `data.templates.actions[].in_person_email` | string | no | Host email for in-person signing roles. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "status": "string",
      "templates": {
        "actions": [
          {}
        ],
        "createdTime": 1,
        "description": "string",
        "documentIds": [
          {}
        ],
        "emailReminders": true,
        "expirationDays": 1,
        "isSequential": true,
        "modifiedTime": 1,
        "notes": "string",
        "ownerEmail": "ava@example.com",
        "requestTypeId": "string",
        "requestTypeName": "Ava Chen",
        "templateId": "string",
        "templateName": "Ava Chen"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `status` | string |  |
| `templates` | object |  |
| `templates.actions` | array<object> |  |
| `templates.createdTime` | number |  |
| `templates.description` | string |  |
| `templates.documentIds` | array<object> |  |
| `templates.emailReminders` | boolean |  |
| `templates.expirationDays` | number |  |
| `templates.isSequential` | boolean |  |
| `templates.modifiedTime` | number |  |
| `templates.notes` | string |  |
| `templates.ownerEmail` | string |  |
| `templates.requestTypeId` | string |  |
| `templates.requestTypeName` | string |  |
| `templates.templateId` | string |  |
| `templates.templateName` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `POST /templates` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

