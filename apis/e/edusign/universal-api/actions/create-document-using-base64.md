# Edusign: Create Document Using Base64

Creates a new document in Edusign from Base64.

```
POST https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-document-using-base64
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-document-using-base64" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "sendDocumentToSignByEmail": "ava@example.com",
  "sendDocumentByEmailWhenCompleted": "ava@example.com",
  "signatureValidationMethod": "string",
  "signWithOrder": true,
  "sendCustomDocumentEmail.subject": "ava@example.com",
  "sendCustomDocumentEmail.body": "ava@example.com",
  "sendCustomSignatureReminderEmail.subject": "ava@example.com",
  "sendCustomSignatureReminderEmail.body": "ava@example.com",
  "sendCustomSignatureReminderEmail.amount": 1,
  "sendCustomSignatureReminderEmail.interval": 1,
  "sendCustomEmailWhenDocumentCompleted.subject": "ava@example.com",
  "sendCustomEmailWhenDocumentCompleted.body": "ava@example.com",
  "adminId": "string",
  "recipients[]": [
    [
      "string"
    ]
  ],
  "inputs[]": [
    {}
  ],
  "document": {},
  "document.name": "Ava Chen",
  "document.base64": "string",
  "attachedDocuments[].name": "Ava Chen",
  "attachedDocuments[].url": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/edusign/latest/actions/create-document-using-base64', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "sendDocumentToSignByEmail": "ava@example.com",
    "sendDocumentByEmailWhenCompleted": "ava@example.com",
    "signatureValidationMethod": "string",
    "signWithOrder": true,
    "sendCustomDocumentEmail.subject": "ava@example.com",
    "sendCustomDocumentEmail.body": "ava@example.com",
    "sendCustomSignatureReminderEmail.subject": "ava@example.com",
    "sendCustomSignatureReminderEmail.body": "ava@example.com",
    "sendCustomSignatureReminderEmail.amount": 1,
    "sendCustomSignatureReminderEmail.interval": 1,
    "sendCustomEmailWhenDocumentCompleted.subject": "ava@example.com",
    "sendCustomEmailWhenDocumentCompleted.body": "ava@example.com",
    "adminId": "string",
    "recipients[]": [["string"]],
    "inputs[]": [{}],
    "document": {},
    "document.name": "Ava Chen",
    "document.base64": "string",
    "attachedDocuments[].name": "Ava Chen",
    "attachedDocuments[].url": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `directoryId` | string | no | Sélectionnez le dossier existant dans lequel vous souhaitez enregistrer les documents que vous créez |
| `trainingId` | string | no | This field is used to select the existing training in which you want to link the documents you are creating |
| `sendDocumentToSignByEmail` | string | yes | This field is used to choose if the document should be sent by email to all recipients to allow them to sign it. Default: true |
| `sendDocumentByEmailWhenCompleted` | string | yes | This field is used to choose if the document should be sent by email to all recipients once it is fully signed. Default: true |
| `redirectionLinkOnceSigned` | string | no | Redirigez l'utilisateur vers une URL spécifique une fois qu'il a signé |
| `signatureValidationMethod` | string | yes | Allowed values: "email", "sms", "none" (none make the signature validation optional). Default: "email" |
| `signWithOrder` | boolean | yes | This field allows to send the document to the recipients one after the other only when the previous recipient has signed |
| `expirationDate` | string | no | This field allows you to define a date from which it will no longer be possible to sign the document |
| `attachedDocuments[]` | array<object> | no |  |
| `sendCustomDocumentEmail` | object | no |  |
| `sendCustomDocumentEmail.subject` | string | yes | The subject of the email |
| `sendCustomDocumentEmail.body` | string | yes | The body of the email |
| `sendCustomSignatureReminderEmail` | object | no |  |
| `sendCustomSignatureReminderEmail.subject` | string | yes | The subject of the email |
| `sendCustomSignatureReminderEmail.body` | string | yes | The body of the email |
| `sendCustomSignatureReminderEmail.amount` | number | yes | The number of reminder emails you want to send |
| `sendCustomSignatureReminderEmail.interval` | number | yes | The interval in hours between each reminder email (in hours) |
| `sendCustomEmailWhenDocumentCompleted` | object | no |  |
| `sendCustomEmailWhenDocumentCompleted.subject` | string | yes | The subject of the email |
| `sendCustomEmailWhenDocumentCompleted.body` | string | yes | The body of the email |
| `adminId` | string | yes | The ID of the admin who sends the document |
| `recipients[]` | array<array> | yes | An array containing arrays of recipients for each document to be sent <br> Each array of recipients represents a document that will be sent. All recipient arrays must be identical (same number of recipients in the same order), only the IDs must be different from one array to another <strong style="color:gold">WARNING</strong> : All recipient arrays must be identical (same number of recipients in the same order), only the IDs must be different from one array to another |
| `inputs[]` | array<object> | yes |  |
| `document` | object | yes | The document you want to send |
| `document.name` | string | yes | The name of the document |
| `document.base64` | string | yes | The base64 string of the document |
| `useNativeCoordinates` | boolean | no | This field allows you to use native coordinates for the document? If true, the coordinates will be used as is, if false, the coordinates will be scaled to the document size |
| `attachedDocuments[].name` | string | yes | Nom du document joint |
| `attachedDocuments[].url` | string | yes | URL du document joint |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "directoryId": "string",
        "documents": [
          {
            "id": "string",
            "signatureLinks": [
              {
                "signatoryEmail": "ava@example.com",
                "signatoryId": "https://example.com",
                "signatureLink": "https://example.com"
              }
            ]
          }
        ],
        "documentsSuccess": 1
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
| `result` | object |  |
| `result.directoryId` | string |  |
| `result.documents` | array<object> |  |
| `result.documents[].id` | string |  |
| `result.documents[].signatureLinks` | array<object> |  |
| `result.documents[].signatureLinks[].signatoryEmail` | string |  |
| `result.documents[].signatureLinks[].signatoryId` | string |  |
| `result.documents[].signatureLinks[].signatureLink` | string |  |
| `result.documentsSuccess` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `POST /v2/documents` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-document-using-base64.md) for the provider-specific parameters and requirements.

