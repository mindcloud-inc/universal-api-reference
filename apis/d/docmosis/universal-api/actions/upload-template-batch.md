# Docmosis: Upload Template Batch



```
POST https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-template-batch
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-template-batch" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateZip": "Upload a .zip file of templates"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/upload-template-batch', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateZip": "Upload a .zip file of templates"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `templateZip` | file | yes | Zip file containing the templates to upload. Example: `Upload a .zip file of templates`. |
| `intoFolder` | string | no | Upload the templates into this environment folder path. Example: `stage3/docmosis/templates`. |
| `userJobId` | string | no | Optional batch upload job identifier used for status and cancel calls. Example: `docmosis-stage3-batch-001`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `devMode` | boolean | no | Upload templates in developer mode, allowing template errors. Default: `true`. |
| `keepPrevOnFail` | boolean | no | Keep the previous template when a replacement upload fails in non-developer mode. |
| `fieldDelimPrefix` | string | no | Prefix delimiter for plain text merge fields. Example: `<<`. |
| `fieldDelimSuffix` | string | no | Suffix delimiter for plain text merge fields. Example: `>>`. |
| `normalizeTemplateName` | boolean | no | Normalize uploaded template names using Unicode NFC. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "jobStatus": {},
      "longMsg": "string",
      "shortMsg": "string",
      "succeeded": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `jobStatus` | object | Job status details for the batch upload. |
| `longMsg` | string | Detailed status message from Docmosis. |
| `shortMsg` | string | Short status message from Docmosis. |
| `succeeded` | boolean | Whether the batch upload request succeeded. |

## Native endpoint

Through the native Docmosis API, this operation is `POST /uploadTemplateBatch` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/upload-template-batch.md) for the provider-specific parameters and requirements.

