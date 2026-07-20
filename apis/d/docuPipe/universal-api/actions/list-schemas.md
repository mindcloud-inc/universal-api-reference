# DocuPipe: List Schemas

Retrieves schemas from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-schemas
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-schemas?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/list-schemas?${params}`, {
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
| `excludePayload` | boolean | no | Whether to exclude the jsonSchema payload Default: `true`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "guidelines": "string",
      "jobId": "string",
      "jsonSchema": {},
      "schemaId": "string",
      "schemaName": "Ava Chen",
      "timestamp": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `guidelines` | string | Guidelines for the schema. |
| `jobId` | string | Unique identifier of the job that last modified the schema. |
| `jsonSchema` | object | The JSON schema that defines the structure of the data. |
| `schemaId` | string | Unique identifier of the schema. |
| `schemaName` | string | Name of the schema. |
| `timestamp` | string | Timestamp of the schema creation. |

## Native endpoint

Through the native DocuPipe API, this operation is `GET /schemas` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-schemas.md) for the provider-specific parameters and requirements.

