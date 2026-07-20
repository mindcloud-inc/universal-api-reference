# DocuPanda - Document Understanding: List Schemas

Retrieves schemas from DocuPanda.

```
GET https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPanda - Document Understanding `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-schemas?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPandaDocumentUnderstanding/latest/actions/list-schemas?${params}`, {
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
| `limit` | number | no | The maximum number of schemas to return. Maximum is 1000 |
| `offset` | number | no | The number of schemas to skip (to paginate through the data) |
| `exclude_payload` | boolean | no | Whether to exclude the jsonSchema payload |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guidelines": "string",
      "jsonSchema": {},
      "schemaId": "string",
      "schemaName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guidelines` | string | Guidelines for the schema. |
| `jsonSchema` | object | The JSON schema that defines the structure of the data. |
| `schemaId` | string | Unique identifier of the schema. |
| `schemaName` | string | Name of the schema. |

## Native endpoint

Through the native DocuPanda - Document Understanding API, this operation is `GET /schemas` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-schemas.md) for the provider-specific parameters and requirements.

