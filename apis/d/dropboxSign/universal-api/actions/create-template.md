# Dropbox Sign: Create Template

Creates a template in Dropbox Sign.

```
POST https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/create-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dropbox Sign `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/create-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file_urls[]": [
    "https://example.com"
  ],
  "title": "string",
  "signer_roles[].name": "Ava Chen",
  "signer_roles[].order": 1,
  "form_fields_per_document[].document_index": 1,
  "form_fields_per_document[].api_id": "string",
  "form_fields_per_document[].type": "string",
  "form_fields_per_document[].required": true,
  "form_fields_per_document[].signer": "string",
  "form_fields_per_document[].width": 1,
  "form_fields_per_document[].height": 1,
  "form_fields_per_document[].x": 1,
  "form_fields_per_document[].y": 1,
  "form_fields_per_document[].page": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dropboxSign/latest/actions/create-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file_urls[]": ["https://example.com"],
    "title": "string",
    "signer_roles[].name": "Ava Chen",
    "signer_roles[].order": 1,
    "form_fields_per_document[].document_index": 1,
    "form_fields_per_document[].api_id": "string",
    "form_fields_per_document[].type": "string",
    "form_fields_per_document[].required": true,
    "form_fields_per_document[].signer": "string",
    "form_fields_per_document[].width": 1,
    "form_fields_per_document[].height": 1,
    "form_fields_per_document[].x": 1,
    "form_fields_per_document[].y": 1,
    "form_fields_per_document[].page": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `file_urls[]` | array<string> | yes | Public file URLs Dropbox Sign should download for the template. |
| `title` | string | yes | Template title. |
| `subject` | string | no | Default template email subject. |
| `message` | string | no | Default template email message. |
| `test_mode` | boolean | no | Whether the template should be created in test mode. |
| `signer_roles[].name` | string | yes | Signer role name. |
| `signer_roles[].order` | number | yes | Signer role order. |
| `form_fields_per_document[].document_index` | number | yes | Document index for the form field. |
| `form_fields_per_document[].api_id` | string | yes | Unique API id for the form field. |
| `form_fields_per_document[].type` | string | yes | Form field type. |
| `form_fields_per_document[].required` | boolean | yes | Whether the field is required. |
| `form_fields_per_document[].signer` | string | yes | Signer index for the field. |
| `form_fields_per_document[].width` | number | yes | Field width. |
| `form_fields_per_document[].height` | number | yes | Field height. |
| `form_fields_per_document[].x` | number | yes | Field x coordinate. |
| `form_fields_per_document[].y` | number | yes | Field y coordinate. |
| `form_fields_per_document[].page` | number | yes | Field page number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "template": {
        "templateId": "string"
      },
      "warnings": [
        {
          "warningMsg": "string",
          "warningName": "Ava Chen"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `template.templateId` | string |  |
| `warnings[].warningMsg` | string |  |
| `warnings[].warningName` | string |  |

## Native endpoint

Through the native Dropbox Sign API, this operation is `POST /template/create` (base URL `https://api.hellosign.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-template.md) for the provider-specific parameters and requirements.

