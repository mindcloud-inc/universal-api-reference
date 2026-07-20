# PdfFiller: List Filled Forms

Retrieves filled forms from a PdfFiller fill request.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-filled-forms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-filled-forms?connectionId=$CONNECTION_ID&linkToFillId=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkToFillId": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/list-filled-forms?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "current_page": 1,
      "items": [
        {
          "additional_documents": [
            {
              "files": [
                {
                  "date_created": "string",
                  "filename": "Ava Chen",
                  "id": 1,
                  "ip": "string"
                }
              ],
              "name": "Ava Chen"
            }
          ],
          "date": 1,
          "document_id": 1,
          "email": "ava@example.com",
          "filled_form_id": 1,
          "ip": "string",
          "name": "Ava Chen",
          "reusable_document_id": 1,
          "signature_stamp": true,
          "token": [
            {
              "data": [
                {
                  "key_1": "string",
                  "key_2": "string",
                  "key_3": 1
                }
              ],
              "hash": "string",
              "id": 1
            }
          ]
        }
      ],
      "next_page_url": "https://example.com",
      "per_page": 1,
      "prev_page_url": "https://example.com",
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `current_page` | number |  |
| `items[].additional_documents[].files[].date_created` | string |  |
| `items[].additional_documents[].files[].filename` | string |  |
| `items[].additional_documents[].files[].id` | number |  |
| `items[].additional_documents[].files[].ip` | string |  |
| `items[].additional_documents[].name` | string |  |
| `items[].date` | number |  |
| `items[].document_id` | number |  |
| `items[].email` | string |  |
| `items[].filled_form_id` | number |  |
| `items[].ip` | string |  |
| `items[].name` | string |  |
| `items[].reusable_document_id` | number |  |
| `items[].signature_stamp` | boolean |  |
| `items[].token[].data[].key_1` | string |  |
| `items[].token[].data[].key_2` | string |  |
| `items[].token[].data[].key_3` | number |  |
| `items[].token[].hash` | string |  |
| `items[].token[].id` | number |  |
| `next_page_url` | string |  |
| `per_page` | number |  |
| `prev_page_url` | string |  |
| `total` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/fillable_forms/:linkToFillId/filled_forms` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-filled-forms.md) for the provider-specific parameters and requirements.

