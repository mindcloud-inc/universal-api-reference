# DocuPipe: Retrieve a Schema

Retrieves a schema from DocuPipe.

```
GET https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-schema
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-schema?connectionId=$CONNECTION_ID&schemaId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "schemaId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/retrieve-a-schema?${params}`, {
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
| `schemaId` | string | yes |  |

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

Through the native DocuPipe API, this operation is `GET /schema/:schemaId` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-a-schema.md) for the provider-specific parameters and requirements.

