# DocuPanda - Document Understanding: Edit a Schema

Updates an existing schema in DocuPanda.

```
PUT https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-edit-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-edit-schema" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "schemaId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/post-edit-schema', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "schemaId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `description` | string | no | New description to assign to the schema. |
| `guidelines` | string | no | New guidelines to assign to the schema. |
| `schemaId` | string | yes | Unique identifier of the schema which we are editing. |
| `schemaName` | string | no | New name to assign to the schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `success` | boolean | Whether the schema was successfully edited. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `POST /schema/edit` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/post-edit-schema.md) for the provider-specific parameters and requirements.

