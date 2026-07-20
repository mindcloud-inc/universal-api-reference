# Veryfi: Update a âDoc

Updates an existing AnyDoc in Veryfi.

```
PUT https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-any-documents-document-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Veryfi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-any-documents-document-id" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "documentId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/veryfi/latest/actions/put-api-v8-partner-any-documents-document-id', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "documentId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `documentId` | string | yes |  |
| `externalId` | string | no | Possible values: non-empty Deprecated 2025-01-09, use meta.external_id instead. |
| `meta` | string | no | Possible values: non-empty Possible values: non-empty Default value: `` |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blueprint_name": "Ava Chen",
      "created_date": "string",
      "external_id": "string",
      "id": 1,
      "img_thumbnail_url": "https://example.com",
      "meta": "string",
      "pdf_url": "https://example.com",
      "property name*": "Ava Chen",
      "template_name": "Ava Chen",
      "text": "string",
      "updated_date": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blueprint_name` | string |  |
| `created_date` | string |  |
| `external_id` | string |  |
| `id` | number |  |
| `img_thumbnail_url` | string |  |
| `meta` | string |  |
| `pdf_url` | string |  |
| `property name*` | string |  |
| `template_name` | string |  |
| `text` | string |  |
| `updated_date` | string |  |

## Native endpoint

Through the native Veryfi API, this operation is `PUT /api/v8/partner/any-documents/:document_id` (base URL `https://api.veryfi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/put-api-v8-partner-any-documents-document-id.md) for the provider-specific parameters and requirements.

