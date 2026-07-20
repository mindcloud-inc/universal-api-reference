# PdfFiller: List Template Fields

Retrieves fields for a PdfFiller template.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-template-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-template-fields?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-template-fields?${params}`, {
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
| `templateId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "allowCustomText": true,
      "fillable": true,
      "format": "string",
      "initial": "string",
      "label": "string",
      "list": [
        "string"
      ],
      "maxChars": 1,
      "maxLines": 1,
      "name": "Ava Chen",
      "radioGroup": "string",
      "required": true,
      "type": "string",
      "value": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `allowCustomText` | boolean |  |
| `fillable` | boolean |  |
| `format` | string |  |
| `initial` | string |  |
| `label` | string |  |
| `list` | array<string> |  |
| `maxChars` | number |  |
| `maxLines` | number |  |
| `name` | string |  |
| `radioGroup` | string |  |
| `required` | boolean |  |
| `type` | string |  |
| `value` | string |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/templates/:templateId/fields` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-template-fields.md) for the provider-specific parameters and requirements.

