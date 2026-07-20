# PdfFiller: Export Filled Form Data

Retrieves exported data for a filled form in PdfFiller.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/export-filled-form-data
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/export-filled-form-data?connectionId=$CONNECTION_ID&linkToFillId=https%3A%2F%2Fexample.com&filledFormId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkToFillId": "https://example.com",
  "filledFormId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/export-filled-form-data?${params}`, {
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
| `linkToFillId` | string | yes |  |
| `filledFormId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "date": "string",
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "pages": [
        {
          "fillable_fields_num": 1,
          "fillable_fields": [
            {
              "content": "string",
              "name": "Ava Chen"
            }
          ],
          "integer": 1,
          "prefilled_content_num": 1
        }
      ],
      "status": "string",
      "time": "string",
      "total_pages": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `date` | string |  |
| `email` | string |  |
| `id` | string |  |
| `name` | string |  |
| `pages[].fillable_fields_num` | number |  |
| `pages[].fillable_fields[].content` | string |  |
| `pages[].fillable_fields[].name` | string |  |
| `pages[].integer` | number |  |
| `pages[].prefilled_content_num` | number |  |
| `status` | string |  |
| `time` | string |  |
| `total_pages` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/fillable_forms/:linkToFillId/filled_forms/:filledFormId/export` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/export-filled-form-data.md) for the provider-specific parameters and requirements.

