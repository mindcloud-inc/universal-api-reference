# Zoho Sign: Submit Document

Submits a document for signature in Zoho Sign.

```
PUT https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/submit-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/submit-document" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "requestId": "string",
  "data": {},
  "data.requests": {},
  "data.requests.actions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoSign/latest/actions/submit-document', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "requestId": "string",
    "data": {},
    "data.requests": {},
    "data.requests.actions[]": [{}]
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `requestId` | string | yes | Zoho Sign request identifier. |
| `data` | object | yes | Zoho Sign submit payload wrapper. |
| `data.requests` | object | yes | Submit request details. |
| `data.requests.actions[]` | array<object> | yes | Recipient rows to submit for signature. |
| `data.requests.actions[].actionId` | string | no | Existing Zoho Sign action identifier for the recipient row. |
| `data.requests.actions[].actionType` | string | no | Recipient action type such as SIGN. |
| `data.requests.actions[].signingOrder` | number | no | Sequential order number for the recipient. |
| `data.requests.actions[].verifyRecipient` | boolean | no | Whether Zoho Sign should verify the recipient before signing. |
| `data.requests.actions[].privateNotes` | string | no | Private instructions shown to the recipient. |
| `data.requests.actions[].fields[]` | array<object> | no | Fields assigned to the recipient. |
| `data.requests.actions[].fields[].fieldTypeName` | string | no | Zoho Sign field type name. |
| `data.requests.actions[].fields[].fieldCategory` | string | no | Field category such as textfield. |
| `data.requests.actions[].fields[].fieldLabel` | string | no | User-facing field label. |
| `data.requests.actions[].fields[].fieldName` | string | no | Internal field name. |
| `data.requests.actions[].fields[].isMandatory` | boolean | no | Whether the field must be completed. |
| `data.requests.actions[].fields[].pageNo` | number | no | Zero-based or provider page index for the field placement. |
| `data.requests.actions[].fields[].documentId` | string | no | Zoho Sign document identifier for the field placement. |
| `data.requests.actions[].fields[].actionId` | string | no | Recipient action identifier associated with the field. |
| `data.requests.actions[].fields[].xCoord` | number | no | Horizontal field position. |
| `data.requests.actions[].fields[].yCoord` | number | no | Vertical field position. |
| `data.requests.actions[].fields[].absHeight` | number | no | Absolute field height. |
| `data.requests.actions[].fields[].absWidth` | number | no | Absolute field width. |
| `data.requests.actions[].fields[].textProperty` | object | no | Text styling properties for supported field types. |
| `data.requests.actions[].fields[].textProperty.font` | string | no | Font family for the field text. |
| `data.requests.actions[].fields[].textProperty.fontSize` | number | no | Font size for the field text. |
| `data.requests.actions[].fields[].textProperty.fontColor` | string | no | Font color for the field text. |
| `data.requests.actions[].fields[].textProperty.maxFieldLength` | number | no | Maximum allowed field length. |
| `data.requests.actions[].fields[].textProperty.isBold` | boolean | no | Whether the field text is bold. |
| `data.requests.actions[].fields[].textProperty.isItalic` | boolean | no | Whether the field text is italic. |

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

Through the native Zoho Sign API, this operation is `POST /requests/:requestId/submit` (base URL `https://sign.zoho.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/submit-document.md) for the provider-specific parameters and requirements.

