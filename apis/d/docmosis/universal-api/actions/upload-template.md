# Docmosis: Upload Template



```
POST https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateFile": "https://resources.docmosis.com/Integrations/FormAssembly/LetterTemplateForFormAssembly.docx"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateFile": "https://resources.docmosis.com/Integrations/FormAssembly/LetterTemplateForFormAssembly.docx"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateFile` | file | yes | The DOCX template file to upload. Example: `https://resources.docmosis.com/Integrations/FormAssembly/LetterTemplateForFormAssembly.docx`. |
| `templateName` | string | no | Optional overriding template path and file name. Example: `/mindcloud/stage3/docmosis-stage3-template.docx`. |
| `templateDescription` | string | no | Optional description stored with the uploaded template. Example: `MindCloud Stage 3 template`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `devMode` | boolean | no | Whether to upload in developer mode. Example: `true`. |
| `keepPrevOnFail` | boolean | no | Whether to keep the previous template when a non-dev upload fails. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "shortMsg": "string",
      "succeeded": true,
      "templateDetails": {
        "isSystemTemplate": "string",
        "lastModifiedISO8601": "string",
        "lastModifiedMillisSinceEpoch": "string",
        "md5": "string",
        "name": "Ava Chen",
        "sizeBytes": "string",
        "templateDescription": "string",
        "templateDevMode": "string",
        "templateHasErrors": "string",
        "templatePlainTextFieldPrefix": "string",
        "templatePlainTextFieldSuffix": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shortMsg` | string |  |
| `succeeded` | boolean |  |
| `templateDetails.isSystemTemplate` | string |  |
| `templateDetails.lastModifiedISO8601` | string |  |
| `templateDetails.lastModifiedMillisSinceEpoch` | string |  |
| `templateDetails.md5` | string |  |
| `templateDetails.name` | string |  |
| `templateDetails.sizeBytes` | string |  |
| `templateDetails.templateDescription` | string |  |
| `templateDetails.templateDevMode` | string |  |
| `templateDetails.templateHasErrors` | string |  |
| `templateDetails.templatePlainTextFieldPrefix` | string |  |
| `templateDetails.templatePlainTextFieldSuffix` | string |  |

## Native endpoint

Through the native Docmosis API, this operation is `POST /uploadTemplate` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-template.md) for the provider-specific parameters and requirements.

