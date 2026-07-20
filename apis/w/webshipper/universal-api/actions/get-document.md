# Webshipper: Get Document

Retrieves a document from Webshipper.

```
GET https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/get-document
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Webshipper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/get-document?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/webshipper/latest/actions/get-document?${params}`, {
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
| `id` | string | no | The document ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "description": "string",
      "document_format": "string",
      "document_size": "string",
      "document_type": "string",
      "id": "string",
      "is_paperless": true,
      "is_special": true,
      "name": "Ava Chen",
      "shipment_id": 1,
      "type": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `description` | string |  |
| `document_format` | string |  |
| `document_size` | string |  |
| `document_type` | string |  |
| `id` | string |  |
| `is_paperless` | boolean |  |
| `is_special` | boolean |  |
| `name` | string |  |
| `shipment_id` | number |  |
| `type` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Webshipper API, this operation is `GET /documents/:id` (base URL `https://{{credentials.accountName}}.api.webshipper.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-document.md) for the provider-specific parameters and requirements.

