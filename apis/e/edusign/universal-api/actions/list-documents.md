# Edusign: List Documents

Retrieves documents from Edusign.

```
GET https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-documents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Edusign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-documents?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/edusign/latest/actions/list-documents?${params}`, {
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
| `offset` | string | no | Query param for pagination, starts at page "0" and displays "limit" documents per page, with a maximum of 500. |
| `limit` | string | no | Query param for pagination, maximum of 500 documents per page. |
| `recipientId` | string | no | Retrieve documents based on a recipient resource ID : - Student ID - Professor ID - External ID - Admin ID (a user with the 'admin' rights in Edusign) |
| `state` | string | no | Retrieve documents based on its signature state : - "completed" : All recipients have signed the document - "pending" : At least one signature is still pending - "expired" : The signature link is no longer available - "refused" : The recipient(s) have refused to sign |
| `createdAfter` | string | no | Retrieve documents created after the provided date (format YYYY-MM-DDThh:mm:ss, ISO 8601) |
| `createdBefore` | string | no | Retrieve documents created before the provided date (format YYYY-MM-DDThh:mm:ss, ISO 8601) |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `getHtml` | string | no | Retrieve or not the HTML version of the document. <strong style="color:gold">WARNING</strong> : The weight of the HTML template can have an impact on the payload size and request speed, depending on the quantity of documents to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "result": {
        "documents": [
          {
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
          }
        ],
        "total": 1
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
| `result.documents` | array<object> |  |
| `result.documents[].adminId` | string |  |
| `result.documents[].automaticEmailSend` | boolean |  |
| `result.documents[].dateCreated` | string |  |
| `result.documents[].dateExpired` | string |  |
| `result.documents[].dateUpdated` | string |  |
| `result.documents[].deletedBy` | string |  |
| `result.documents[].directoryId` | string |  |
| `result.documents[].documentProofUrl` | string |  |
| `result.documents[].documentSecured` | boolean |  |
| `result.documents[].documentSignatureCodes` | array<string> |  |
| `result.documents[].documentUrl` | string |  |
| `result.documents[].id` | string |  |
| `result.documents[].inputs` | array<object> |  |
| `result.documents[].inputs[].category` | string |  |
| `result.documents[].inputs[].id` | string |  |
| `result.documents[].inputs[].label` | string |  |
| `result.documents[].inputs[].personId` | string |  |
| `result.documents[].inputs[].position` | object |  |
| `result.documents[].inputs[].position.height` | number |  |
| `result.documents[].inputs[].position.page` | number |  |
| `result.documents[].inputs[].position.width` | number |  |
| `result.documents[].inputs[].position.x` | number |  |
| `result.documents[].inputs[].position.y` | number |  |
| `result.documents[].inputs[].required` | boolean |  |
| `result.documents[].inputs[].type` | string |  |
| `result.documents[].metadatas` | object |  |
| `result.documents[].metadatas.signatoryDate` | string |  |
| `result.documents[].metadatas.signatoryEmail` | string |  |
| `result.documents[].metadatas.signatoryFullname` | string |  |
| `result.documents[].metadatas.signatoryIp` | string |  |
| `result.documents[].metadatas.signatorySign` | string |  |
| `result.documents[].metadatas.signatoryToken` | string |  |
| `result.documents[].metadatas.signatoryType` | string |  |
| `result.documents[].metadatas.signatoryUrl` | string |  |
| `result.documents[].metadatas.validationCode` | string |  |
| `result.documents[].name` | string |  |
| `result.documents[].professorId` | string |  |
| `result.documents[].schoolId` | string |  |
| `result.documents[].state` | string |  |
| `result.documents[].studentDownloadDocument` | boolean |  |
| `result.documents[].studentId` | string |  |
| `result.documents[].template` | string |  |
| `result.documents[].templateId` | string |  |
| `result.documents[].toDelete` | boolean |  |
| `result.documents[].trainingId` | string |  |
| `result.documents[].type` | number |  |
| `result.documents[].userId` | string |  |
| `result.documents[].variables` | object |  |
| `result.documents[].variables.emails` | object |  |
| `result.documents[].variables.emails.documentCompleted` | object |  |
| `result.documents[].variables.emails.documentCompleted.body` | string |  |
| `result.documents[].variables.emails.documentCompleted.subject` | string |  |
| `result.documents[].variables.emails.documentSent` | object |  |
| `result.documents[].variables.emails.documentSent.body` | string |  |
| `result.documents[].variables.emails.documentSent.subject` | string |  |
| `result.documents[].variables.emails.signatureReminder` | object |  |
| `result.documents[].variables.emails.signatureReminder.amount` | number |  |
| `result.documents[].variables.emails.signatureReminder.body` | string |  |
| `result.documents[].variables.emails.signatureReminder.emailsAlreadySent` | array<string> |  |
| `result.documents[].variables.emails.signatureReminder.interval` | number |  |
| `result.documents[].variables.emails.signatureReminder.subject` | string |  |
| `result.documents[].variables.recipients` | array<object> |  |
| `result.documents[].variables.recipients[].category` | string |  |
| `result.documents[].variables.recipients[].email` | string |  |
| `result.documents[].variables.recipients[].firstname` | string |  |
| `result.documents[].variables.recipients[].id` | string |  |
| `result.documents[].variables.recipients[].index` | number |  |
| `result.documents[].variables.recipients[].lastname` | string |  |
| `result.documents[].variables.recipients[].name` | string |  |
| `result.documents[].variables.recipients[].order` | number |  |
| `result.documents[].variables.recipients[].phone` | string |  |
| `result.documents[].variables.recipients[].signatureDate` | string |  |
| `result.documents[].variables.recipients[].signatureState` | string |  |
| `result.documents[].variables.recipients[].signatureUrl` | boolean |  |
| `result.documents[].variables.recipients[].token` | string |  |
| `result.documents[].variables.sendEmailWhenCompleted` | boolean |  |
| `result.documents[].variables.step` | number |  |
| `result.documents[].variables.validationMethod` | string |  |
| `result.documents[].variables.version` | number |  |
| `result.documents[].yousignProcedure` | string |  |
| `result.total` | number |  |
| `status` | string |  |

## Native endpoint

Through the native Edusign API, this operation is `GET /v2/documents` (base URL `https://ext.edusign.fr`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-documents.md) for the provider-specific parameters and requirements.

