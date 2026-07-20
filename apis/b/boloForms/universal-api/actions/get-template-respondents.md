# BoloForms: Get Template Respondents

Retrieves respondents for a BoloForms template.

```
GET https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/get-template-respondents
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoloForms `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/get-template-respondents?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boloForms/latest/actions/get-template-respondents?${params}`, {
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
| `templateId` | string | yes | Template ID to retrieve respondents for |
| `page` | number | no | Page number for pagination |
| `limit` | number | no | Number of respondents per page |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `respondentDocumentId` | string | no | Specific respondent ID to retrieve |

## Response

```json
{
  "success": true,
  "data": [
    {
      "createdAt": "string",
      "finishedPdfUrl": "https://example.com",
      "history": [
        {}
      ],
      "ownerId": "string",
      "pdfLink": "https://example.com",
      "respondentDocumentId": "string",
      "signers": [
        {}
      ],
      "status": "string",
      "templateId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `createdAt` | string | Creation timestamp for the respondent document. |
| `finishedPdfUrl` | string | Finished PDF URL when available. |
| `history` | array<object> | Activity history entries for the respondent document. |
| `ownerId` | string | Workspace owner ID for the respondent document. |
| `pdfLink` | string | PDF link for the respondent document. |
| `respondentDocumentId` | string | Respondent document ID returned for the template response. |
| `signers` | array<object> | Signer records for the respondent document. |
| `status` | string | Current respondent document status. |
| `templateId` | string | Template ID associated with the respondent document. |

## Native endpoint

Through the native BoloForms API, this operation is `GET /get-template-respondent` (base URL `https://sapi.boloforms.com/signature`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-respondents.md) for the provider-specific parameters and requirements.

