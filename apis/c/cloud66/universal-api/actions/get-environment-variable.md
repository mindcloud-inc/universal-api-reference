# Cloud 66: Get Environment Variable

Retrieves an environment variable from your Cloud 66 account.

```
GET https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-environment-variable
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloud 66 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-environment-variable?connectionId=$CONNECTION_ID&stackId=string&envVarId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "envVarId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloud66/latest/actions/get-environment-variable?${params}`, {
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
| `envVarId` | number | yes | The environment variable ID |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Cloud 66 API returns.

## Native endpoint

Through the native Cloud 66 API, this operation is `GET /stacks/:stack_id/environments/:env_var_id` (base URL `https://app.cloud66.com/api/3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-environment-variable.md) for the provider-specific parameters and requirements.

