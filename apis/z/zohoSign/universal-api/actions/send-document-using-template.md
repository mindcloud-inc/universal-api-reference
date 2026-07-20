# Zoho Sign: Send Document Using Template

Creates a document from a template in Zoho Sign.

```
POST https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/send-document-using-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/send-document-using-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string",
  "data": {},
  "data.templates": {},
  "data.templates.actions[]": [
    {}
  ],
  "data.templates.actions[].actionId": "string",
  "data.templates.actions[].recipientName": "Ava Chen",
  "data.templates.actions[].recipientEmail": "ava@example.com",
  "data.templates.actions[].verifyRecipient": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/send-document-using-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string",
    "data": {},
    "data.templates": {},
    "data.templates.actions[]": [{}],
    "data.templates.actions[].actionId": "string",
    "data.templates.actions[].recipientName": "Ava Chen",
    "data.templates.actions[].recipientEmail": "ava@example.com",
    "data.templates.actions[].verifyRecipient": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateId` | string | yes | Zoho Sign template identifier. |
| `data` | object | yes | Zoho Sign template-send payload wrapper. |
| `data.templates` | object | yes | Template send details. |
| `data.templates.requestName` | string | no | Document request name. Defaults to the template name when omitted. |
| `data.templates.actions[]` | array<object> | yes | Recipient rows aligned to the template actions. |
| `data.templates.actions[].actionId` | string | yes | Template action identifier for the recipient row. |
| `data.templates.actions[].actionType` | string | no | Recipient action type such as SIGN. |
| `data.templates.actions[].role` | string | no | Template role name for the recipient row. |
| `data.templates.actions[].recipientName` | string | yes | Recipient full name. |
| `data.templates.actions[].recipientEmail` | string | yes | Recipient email address. |
| `data.templates.actions[].verifyRecipient` | boolean | yes | Whether recipient verification is required. |
| `data.templates.actions[].verificationType` | string | no | Recipient verification mode such as EMAIL. |
| `data.templates.notes` | string | no | Common message sent to all recipients. |
| `isQuicksend` | boolean | no | When true, immediately send the created request for signature. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.templates.fieldData` | object | no | Prefill values for template fields as a JSON object. |
| `data.templates.actions[].inPersonName` | string | no | Host name for in-person signing flows. |
| `data.templates.actions[].inPersonEmail` | string | no | Host email for in-person signing flows. |
| `data.templates.actions[].privateNotes` | string | no | Private instructions for a specific recipient. |

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

Through the native Zoho Sign API, this operation is `POST /templates/:templateId/createdocument` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-document-using-template.md) for the provider-specific parameters and requirements.

