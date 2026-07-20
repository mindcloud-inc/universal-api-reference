# Shuffler: Get Execution Results

Retrieves execution results from Shuffler.

```
GET https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-execution-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shuffler `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-execution-results?connectionId=$CONNECTION_ID&authorization=string&executionId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "authorization": "string",
  "executionId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shuffler/latest/actions/get-execution-results?${params}`, {
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
| `authorization` | string | yes | Execution authorization token. |
| `executionId` | string | yes | Execution identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "authorization": "string",
      "executionId": "string",
      "result": "string",
      "status": "string",
      "type": "string",
      "workflowId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `authorization` | string |  |
| `executionId` | string |  |
| `result` | string |  |
| `status` | string |  |
| `type` | string |  |
| `workflowId` | string |  |

## Native endpoint

Through the native Shuffler API, this operation is `POST /streams/results` (base URL `https://shuffler.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-execution-results.md) for the provider-specific parameters and requirements.

