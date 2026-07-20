# PdfFiller: Get Template

Retrieves a template from PdfFiller.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/get-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/get-template?connectionId=$CONNECTION_ID&templateId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "templateId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/get-template?${params}`, {
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
      "created": 1,
      "fillable": true,
      "folder": {
        "folder_id": 1,
        "name": "Ava Chen"
      },
      "id": 1,
      "name": "Ava Chen",
      "status": "string",
      "type": "string",
      "updated": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | number |  |
| `fillable` | boolean |  |
| `folder.folder_id` | number |  |
| `folder.name` | string |  |
| `id` | number |  |
| `name` | string |  |
| `status` | string |  |
| `type` | string |  |
| `updated` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/templates/:templateId` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-template.md) for the provider-specific parameters and requirements.

