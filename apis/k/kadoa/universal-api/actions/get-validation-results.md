# Kadoa: Get Validation Results



```
GET https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-validation-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Kadoa `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-validation-results?connectionId=$CONNECTION_ID&jobId=string&workflowId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "jobId": "string",
  "workflowId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/kadoa/latest/actions/get-validation-results?${params}`, {
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
| `jobId` | string | yes | Job ID |
| `workflowId` | string | yes | Workflow ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `includeDryRun` | boolean | no | Include dry run results Default: `false`. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Kadoa API returns.

## Native endpoint

Through the native Kadoa API, this operation is `GET /v4/data-validation/workflows/:workflowId/jobs/:jobId/validations/latest` (base URL `https://api.kadoa.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-validation-results.md) for the provider-specific parameters and requirements.

