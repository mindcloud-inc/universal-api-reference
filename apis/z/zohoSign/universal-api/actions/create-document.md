# Zoho Sign: Create Document

Creates a document in Zoho Sign.

```
POST https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string",
  "data.requests.request_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/create-document', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string",
    "data.requests.request_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file` | file | yes | PDF file to upload for the signature request. |
| `data` | object | no | Zoho Sign request payload wrapper. |
| `data.requests` | object | no | Signature request details. |
| `data.requests.request_name` | string | yes | Display name for the signature request. |
| `data.requests.expiration_days` | number | no | Number of days before the request expires. |
| `data.requests.is_sequential` | boolean | no | Whether recipients must sign in order. |
| `data.requests.email_reminders` | boolean | no | Whether reminder emails are enabled. |
| `data.requests.reminder_period` | number | no | Reminder frequency in days. |
| `data.requests.actions[]` | array<object> | no | Recipients that will act on the document. |
| `data.requests.actions[].recipient_name` | string | no | Recipient display name. |
| `data.requests.actions[].recipient_email` | string | no | Recipient email address. |
| `data.requests.actions[].action_type` | string | no | Recipient action type such as SIGN. |
| `data.requests.actions[].signing_order` | number | no | Sequential order number for the recipient. |
| `data.requests.actions[].verify_recipient` | boolean | no | Whether Zoho Sign should verify the recipient before signing. |
| `data.requests.actions[].verification_type` | string | no | Recipient verification method such as EMAIL. |
| `data.requests.actions[].verification_code` | string | no | Verification code sent to the recipient when required. |
| `data.requests.actions[].private_notes` | string | no | Private instructions shown to the recipient. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "requests": {
        "actions": [
          {}
        ],
        "createdTime": 1,
        "documentIds": [
          {}
        ],
        "emailReminders": true,
        "expirationDays": 1,
        "isSequential": true,
        "modifiedTime": 1,
        "ownerEmail": "ava@example.com",
        "requestId": "string",
        "requestName": "Ava Chen",
        "requestStatus": "string",
        "requestTypeId": "string",
        "requestTypeName": "Ava Chen",
        "selfSign": true,
        "signPercentage": 1
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
| `code` | number |  |
| `message` | string |  |
| `requests` | object |  |
| `requests.actions` | array<object> |  |
| `requests.createdTime` | number |  |
| `requests.documentIds` | array<object> |  |
| `requests.emailReminders` | boolean |  |
| `requests.expirationDays` | number |  |
| `requests.isSequential` | boolean |  |
| `requests.modifiedTime` | number |  |
| `requests.ownerEmail` | string |  |
| `requests.requestId` | string |  |
| `requests.requestName` | string |  |
| `requests.requestStatus` | string |  |
| `requests.requestTypeId` | string |  |
| `requests.requestTypeName` | string |  |
| `requests.selfSign` | boolean |  |
| `requests.signPercentage` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Zoho Sign API, this operation is `POST /requests` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document.md) for the provider-specific parameters and requirements.

