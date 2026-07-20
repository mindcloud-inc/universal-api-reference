# DocuPipe: Copy a Schema to Another Workspace

Copies a schema to another DocuPipe workspace.

```
POST https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/copy-a-schema-to-another-workspace
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DocuPipe `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/copy-a-schema-to-another-workspace" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "schemaId": "string",
  "targetWorkspaceApiKey": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/docuPipe/latest/actions/copy-a-schema-to-another-workspace', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "schemaId": "string",
    "targetWorkspaceApiKey": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `schemaId` | string | yes | Unique identifier of the schema to copy. |
| `targetWorkspaceApiKey` | string | yes | API key of the target workspace to copy the schema to. |

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

Through the native DocuPipe API, this operation is `POST /copy/schema` (base URL `https://app.docupipe.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/copy-a-schema-to-another-workspace.md) for the provider-specific parameters and requirements.

