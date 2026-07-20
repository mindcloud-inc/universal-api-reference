# PdfFiller: Get Filled Form

Retrieves a filled form from PdfFiller.

```
GET https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/get-filled-form
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PdfFiller `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/get-filled-form?connectionId=$CONNECTION_ID&linkToFillId=https%3A%2F%2Fexample.com&filledFormId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "linkToFillId": "https://example.com",
  "filledFormId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pdfFiller/latest/actions/get-filled-form?${params}`, {
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
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `additional_documents[].files[].date_created` | string |  |
| `additional_documents[].files[].filename` | string |  |
| `additional_documents[].files[].id` | number |  |
| `additional_documents[].files[].ip` | string |  |
| `additional_documents[].name` | string |  |
| `date` | number |  |
| `document_id` | number |  |
| `email` | string |  |
| `filled_form_id` | number |  |
| `ip` | string |  |
| `name` | string |  |
| `reusable_document_id` | number |  |
| `signature_stamp` | boolean |  |
| `token[].data[].key_1` | string |  |
| `token[].data[].key_2` | string |  |
| `token[].data[].key_3` | number |  |
| `token[].hash` | string |  |
| `token[].id` | number |  |

## Native endpoint

Through the native PdfFiller API, this operation is `GET /v2/fillable_forms/:linkToFillId/filled_forms/:filledFormId` (base URL `https://api.pdffiller.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-filled-form.md) for the provider-specific parameters and requirements.

