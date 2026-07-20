# Appwrite: Delete execution

Deletes the execution from your Appwrite project.

```
DELETE https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-delete-execution
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Appwrite `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-delete-execution?connectionId=$CONNECTION_ID&functionId=string&executionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "functionId": "string",
  "executionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/appwrite/latest/actions/functions-delete-execution?${params}`, {
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
| `functionId` | string | yes | Function ID. |
| `executionId` | string | yes | Execution ID. |

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
| `success` | boolean | True when the request succeeds. |

## Native endpoint

Through the native Appwrite API, this operation is `DELETE /functions/{functionId}/executions/{executionId}` (base URL `https://cloud.appwrite.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/functions-delete-execution.md) for the provider-specific parameters and requirements.

