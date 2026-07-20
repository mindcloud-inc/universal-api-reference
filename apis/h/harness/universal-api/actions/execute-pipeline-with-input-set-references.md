# Harness: Execute Pipeline With Input Set References

Executes a Harness pipeline with input set references.

```
POST https://connect.mindcloud.co/v1/universal/harness/latest/actions/execute-pipeline-with-input-set-references
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/harness/latest/actions/execute-pipeline-with-input-set-references" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inputSetIdentifier": "string",
  "pipelineIdentifier": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/harness/latest/actions/execute-pipeline-with-input-set-references', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inputSetIdentifier": "string",
    "pipelineIdentifier": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `inputSetIdentifier` | string | yes | Referenced input set identifier. |
| `pipelineIdentifier` | string | yes | Pipeline identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "correlationId": "string",
      "data": {},
      "metaData": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `correlationId` | string | Harness correlation identifier. |
| `data` | object | Pipeline execution payload. |
| `metaData` | object | Optional Harness metadata. |
| `status` | string | Harness API status. |

## Native endpoint

Through the native Harness API, this operation is `POST https://app.harness.io/pipeline/api/pipeline/execute/:pipelineIdentifier/inputSetList?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/execute-pipeline-with-input-set-references.md) for the provider-specific parameters and requirements.

