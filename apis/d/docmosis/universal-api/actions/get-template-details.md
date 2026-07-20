# Docmosis: Get Template Details



```
GET https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-template-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-template-details?connectionId=$CONNECTION_ID&templateName=%2Fmindcloud%2Fstage3%2Fdocmosis-stage3-template.docx" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateName": "/mindcloud/stage3/docmosis-stage3-template.docx"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-template-details?${params}`, {
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
| `templateName` | string | yes | The name of the template to inspect. Example: `/mindcloud/stage3/docmosis-stage3-template.docx`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stringify` | boolean | no | Whether to stringify the JSON result. Example: `false`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "longMsg": "string",
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
| `longMsg` | string |  |
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

Through the native Docmosis API, this operation is `POST /getTemplateDetails` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-details.md) for the provider-specific parameters and requirements.

