# Zoho Sign: Update Document

Updates an existing document in Zoho Sign.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/update-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/update-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/update-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Zoho Sign request identifier. |
| `data` | object | no | Zoho Sign update payload wrapper. |
| `data.requests` | object | no | Updated signature request details. |
| `data.requests.requestName` | string | no | Updated display name for the signature request. |
| `data.requests.notes` | string | no | Notes included with the request. |
| `data.requests.description` | string | no | Description of the request. |
| `data.requests.expirationDays` | number | no | Number of days before the request expires. |
| `data.requests.isSequential` | boolean | no | Whether recipients must sign in order. |
| `data.requests.emailReminders` | boolean | no | Whether reminder emails are enabled. |
| `data.requests.reminderPeriod` | number | no | Reminder frequency in days. |
| `data.requests.validity` | number | no | Validity setting for the request. |
| `data.requests.actions[]` | array<object> | no | Recipients to update on the request. |
| `data.requests.actions[].actionId` | string | no | Existing Zoho Sign action identifier for the recipient row. |
| `data.requests.actions[].recipientName` | string | no | Recipient display name. |
| `data.requests.actions[].recipientEmail` | string | no | Recipient email address. |
| `data.requests.actions[].actionType` | string | no | Recipient action type such as SIGN. |
| `data.requests.actions[].privateNotes` | string | no | Private instructions shown to the recipient. |
| `data.requests.actions[].signingOrder` | number | no | Sequential order number for the recipient. |
| `data.requests.actions[].isBulk` | boolean | no | Whether the recipient row is part of a bulk send. |
| `data.requests.actions[].verifyRecipient` | boolean | no | Whether Zoho Sign should verify the recipient before signing. |

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

Through the native Zoho Sign API, this operation is `PUT /requests/:requestId` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-document.md) for the provider-specific parameters and requirements.

