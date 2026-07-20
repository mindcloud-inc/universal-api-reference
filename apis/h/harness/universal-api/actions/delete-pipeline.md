# Harness: Delete Pipeline

Deletes a pipeline from Harness.

```
DELETE https://connect.mindcloud.co/v1/universal/harness/latest/actions/delete-pipeline
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Harness `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/harness/latest/actions/delete-pipeline?connectionId=$CONNECTION_ID&pipelineIdentifier=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "pipelineIdentifier": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/harness/latest/actions/delete-pipeline?${params}`, {
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
| `pipelineIdentifier` | string | yes | Pipeline identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "correlationId": "string",
      "data": true,
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
| `data` | boolean | Whether the pipeline was deleted. |
| `metaData` | object | Optional Harness metadata. |
| `status` | string | Harness API status. |

## Native endpoint

Through the native Harness API, this operation is `DELETE https://app.harness.io/pipeline/api/pipelines/:pipelineIdentifier?accountIdentifier=:accountIdentifier&orgIdentifier=:orgIdentifier&projectIdentifier=:projectIdentifier` (base URL `https://app.harness.io/gateway`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-pipeline.md) for the provider-specific parameters and requirements.

