# Cloud 66: Delete Environment Variable

Deletes an environment variable from your Cloud 66 account.

```
DELETE https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/delete-environment-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/delete-environment-variable?connectionId=$CONNECTION_ID&stackId=string&envVarKey=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "envVarKey": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/delete-environment-variable?${params}`, {
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
| `stackId` | string | yes | The stack UID |
| `envVarKey` | string | yes | The environment variable key or name |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `DELETE /stacks/:stack_id/environments/:env_var_key` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-environment-variable.md) for the provider-specific parameters and requirements.

