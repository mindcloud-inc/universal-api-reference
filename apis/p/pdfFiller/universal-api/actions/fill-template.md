# PdfFiller: Fill Template

Creates a filled document from a PdfFiller template.

```
POST https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/fill-template
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/fill-template" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "templateId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/fill-template', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "templateId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

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

Through the native PdfFiller API, this operation is `POST /v2/templates/:templateId` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/fill-template.md) for the provider-specific parameters and requirements.

