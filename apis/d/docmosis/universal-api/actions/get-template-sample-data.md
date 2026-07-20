# Docmosis: Get Template Sample Data



```
GET https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-template-sample-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Docmosis `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-template-sample-data?connectionId=$CONNECTION_ID&templateName=%2Fmindcloud%2Fstage3%2Fdocmosis-stage3-template.docx" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateName": "/mindcloud/stage3/docmosis-stage3-template.docx"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docmosis/latest/actions/get-template-sample-data?${params}`, {
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
| `format` | string | no | Response format for sample data. Example: `json`. |

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
        "templateFirstError": "string",
        "templateHasErrors": "string"
      },
      "templateSampleData": {
        "name": "Ava Chen"
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
| `templateDetails.templateFirstError` | string |  |
| `templateDetails.templateHasErrors` | string |  |
| `templateSampleData` | object |  |
| `templateSampleData.name` | string |  |

## Native endpoint

Through the native Docmosis API, this operation is `POST /getSampleData` (base URL `{{credentials.baseUrl}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template-sample-data.md) for the provider-specific parameters and requirements.

