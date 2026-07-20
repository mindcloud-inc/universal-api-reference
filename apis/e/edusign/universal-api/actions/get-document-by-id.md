# Edusign: Get Document By ID

Retrieves a document from Edusign by ID.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-document-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-document-by-id?connectionId=$CONNECTION_ID&documentId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "documentId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/get-document-by-id?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | Document ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "adminId": "string",
        "automaticEmailSend": true,
        "dateCreated": "string",
        "dateExpired": "string",
        "dateUpdated": "string",
        "deletedBy": "string",
        "directoryId": "string",
        "documentProofUrl": "https://example.com",
        "documentSecured": true,
        "documentSignatureCodes": [
          "string"
        ],
        "documentUrl": "https://example.com",
        "id": "string",
        "inputs": [
          {
            "category": "string",
            "id": "string",
            "label": "string",
            "personId": "string",
            "position": {
              "height": 1,
              "page": 1,
              "width": 1,
              "x": 1,
              "y": 1
            },
            "required": true,
            "type": "string"
          }
        ],
        "metadatas": {
          "signatoryDate": "string",
          "signatoryEmail": "ava@example.com",
          "signatoryFullname": "Ava Chen",
          "signatoryIp": "string",
          "signatorySign": "string",
          "signatoryToken": "string",
          "signatoryType": "string",
          "signatoryUrl": "https://example.com",
          "validationCode": "string"
        },
        "name": "Ava Chen",
        "professorId": "string",
        "schoolId": "string",
        "state": "string",
        "studentDownloadDocument": true,
        "studentId": "string",
        "template": "string",
        "templateId": "string",
        "toDelete": true,
        "trainingId": "string",
        "type": 1,
        "userId": "string",
        "variables": {
          "emails": {
            "documentCompleted": {
              "body": "ava@example.com",
              "subject": "ava@example.com"
            },
            "documentSent": {
              "body": "ava@example.com",
              "subject": "ava@example.com"
            },
            "signatureReminder": {
              "amount": 1,
              "body": "ava@example.com",
              "emailsAlreadySent": [
                "ava@example.com"
              ],
              "interval": 1,
              "subject": "ava@example.com"
            }
          },
          "recipients": [
            {
              "category": "string",
              "email": "ava@example.com",
              "firstname": "Ava",
              "id": "string",
              "index": 1,
              "lastname": "Chen",
              "name": "Ava Chen",
              "order": 1,
              "phone": "string",
              "signatureDate": "string",
              "signatureState": "string",
              "signatureUrl": true,
              "token": "string"
            }
          ],
          "sendEmailWhenCompleted": true,
          "step": 1,
          "validationMethod": "string",
          "version": 1
        },
        "yousignProcedure": "string"
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
| `result.adminId` | string |  |
| `result.automaticEmailSend` | boolean |  |
| `result.dateCreated` | string |  |
| `result.dateExpired` | string |  |
| `result.dateUpdated` | string |  |
| `result.deletedBy` | string |  |
| `result.directoryId` | string |  |
| `result.documentProofUrl` | string |  |
| `result.documentSecured` | boolean |  |
| `result.documentSignatureCodes` | array<string> |  |
| `result.documentUrl` | string |  |
| `result.id` | string |  |
| `result.inputs` | array<object> |  |
| `result.inputs[].category` | string |  |
| `result.inputs[].id` | string |  |
| `result.inputs[].label` | string |  |
| `result.inputs[].personId` | string |  |
| `result.inputs[].position` | object |  |
| `result.inputs[].position.height` | number |  |
| `result.inputs[].position.page` | number |  |
| `result.inputs[].position.width` | number |  |
| `result.inputs[].position.x` | number |  |
| `result.inputs[].position.y` | number |  |
| `result.inputs[].required` | boolean |  |
| `result.inputs[].type` | string |  |
| `result.metadatas` | object |  |
| `result.metadatas.signatoryDate` | string |  |
| `result.metadatas.signatoryEmail` | string |  |
| `result.metadatas.signatoryFullname` | string |  |
| `result.metadatas.signatoryIp` | string |  |
| `result.metadatas.signatorySign` | string |  |
| `result.metadatas.signatoryToken` | string |  |
| `result.metadatas.signatoryType` | string |  |
| `result.metadatas.signatoryUrl` | string |  |
| `result.metadatas.validationCode` | string |  |
| `result.name` | string |  |
| `result.professorId` | string |  |
| `result.schoolId` | string |  |
| `result.state` | string |  |
| `result.studentDownloadDocument` | boolean |  |
| `result.studentId` | string |  |
| `result.template` | string |  |
| `result.templateId` | string |  |
| `result.toDelete` | boolean |  |
| `result.trainingId` | string |  |
| `result.type` | number |  |
| `result.userId` | string |  |
| `result.variables` | object |  |
| `result.variables.emails` | object |  |
| `result.variables.emails.documentCompleted` | object |  |
| `result.variables.emails.documentCompleted.body` | string |  |
| `result.variables.emails.documentCompleted.subject` | string |  |
| `result.variables.emails.documentSent` | object |  |
| `result.variables.emails.documentSent.body` | string |  |
| `result.variables.emails.documentSent.subject` | string |  |
| `result.variables.emails.signatureReminder` | object |  |
| `result.variables.emails.signatureReminder.amount` | number |  |
| `result.variables.emails.signatureReminder.body` | string |  |
| `result.variables.emails.signatureReminder.emailsAlreadySent` | array<string> |  |
| `result.variables.emails.signatureReminder.interval` | number |  |
| `result.variables.emails.signatureReminder.subject` | string |  |
| `result.variables.recipients` | array<object> |  |
| `result.variables.recipients[].category` | string |  |
| `result.variables.recipients[].email` | string |  |
| `result.variables.recipients[].firstname` | string |  |
| `result.variables.recipients[].id` | string |  |
| `result.variables.recipients[].index` | number |  |
| `result.variables.recipients[].lastname` | string |  |
| `result.variables.recipients[].name` | string |  |
| `result.variables.recipients[].order` | number |  |
| `result.variables.recipients[].phone` | string |  |
| `result.variables.recipients[].signatureDate` | string |  |
| `result.variables.recipients[].signatureState` | string |  |
| `result.variables.recipients[].signatureUrl` | boolean |  |
| `result.variables.recipients[].token` | string |  |
| `result.variables.sendEmailWhenCompleted` | boolean |  |
| `result.variables.step` | number |  |
| `result.variables.validationMethod` | string |  |
| `result.variables.version` | number |  |
| `result.yousignProcedure` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v2/documents/:documentId` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document-by-id.md) for the provider-specific parameters and requirements.

