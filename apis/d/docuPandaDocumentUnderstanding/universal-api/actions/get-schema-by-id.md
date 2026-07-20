# DocuPanda - Document Understanding: Retrieve a Schema

Retrieves a schema from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-schema-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-schema-by-id?connectionId=$CONNECTION_ID&schema_id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schema_id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/get-schema-by-id?${params}`, {
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
| `schema_id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": "string",
      "message": "string",
      "name": "Ava Chen",
      "status": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string |  |
| `message` | string |  |
| `name` | string |  |
| `status` | array<string> |  |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /schema/id/:schema_id` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-schema-by-id.md) for the provider-specific parameters and requirements.

