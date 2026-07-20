# BoloForms: Send Template For Signing

Sends a BoloForms template for signing.

```
POST https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/send-template-for-signing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoloForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/send-template-for-signing" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string",
  "signingType": "0",
  "receiversList[]": [
    {}
  ],
  "receiversList[].name": "Ava Chen",
  "receiversList[].email": "ava@example.com",
  "customVariables[].varName": "Ava Chen",
  "customVariables[].varValue": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/send-template-for-signing', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string",
    "signingType": "0",
    "receiversList[]": [{}],
    "receiversList[].name": "Ava Chen",
    "receiversList[].email": "ava@example.com",
    "customVariables[].varName": "Ava Chen",
    "customVariables[].varValue": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes | ID of the document template |
| `signingType` | string | yes | Must be PDF_TEMPLATE or FORM_TEMPLATE One of: `0`, `1`. |
| `receiversList[]` | array<object> | yes | List of receivers who need to sign the document |
| `receiversList[].name` | string | yes | Name of the person |
| `receiversList[].email` | string | yes | Email of the person, it will send an email to the customer for signing |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `receiversList[].roleTitle` | string | no | Must exactly match the role added while uploading PDF template in BoloSign dashboard |
| `receiversList[].subject` | string | no | Optional custom subject for this receiver |
| `receiversList[].message` | string | no | Optional custom message for this receiver |
| `mailData` | object | no | Global mail subject and message fallback values |
| `mailData.subject` | string | no | Global subject used when receiver-specific subject is not provided |
| `mailData.message` | string | no | Global message used when receiver-specific message is not provided |
| `customVariables[]` | array<object> | no | Optional custom variables to be replaced in the template |
| `customVariables[].varName` | string | yes | Variable name in square brackets, must match template exactly |
| `customVariables[].varValue` | string | yes | Value to be assigned to the variable |
| `pdfData` | string | no | Base64-encoded PDF data for PDF template sends |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdDocumentId": "string",
      "createdDocumentStatus": "string",
      "message": "string",
      "signers": [
        {}
      ],
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdDocumentId` | string | Created document ID returned for PDF-template sends. |
| `createdDocumentStatus` | string | Created document status returned for PDF-template sends. |
| `message` | string | Provider result message, such as successful send or share status. |
| `signers` | array<object> | Signer records returned for PDF-template sends. |
| `templateId` | string | Template ID echoed for PDF-template sends when returned by the provider. |

## Native endpoint

Through the native BoloForms API, this operation is `POST /pdf-template-lambda` (base URL `https://sapi.boloforms.com/signature`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/send-template-for-signing.md) for the provider-specific parameters and requirements.

