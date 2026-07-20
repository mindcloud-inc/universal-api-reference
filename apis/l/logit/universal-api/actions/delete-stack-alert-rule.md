# Logit: Delete Stack Alert Rule

Deletes an existing stack alert rule from Logit.

```
DELETE https://connect.mindcloud.co/v1/universal/logit/latest/actions/delete-stack-alert-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/logit/latest/actions/delete-stack-alert-rule?connectionId=$CONNECTION_ID&stackId=string&ruleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "ruleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/delete-stack-alert-rule?${params}`, {
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
| `stackId` | string | yes |  |
| `ruleId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Logit API returns.

## Native endpoint

Through the native Logit API, this operation is `DELETE /api/stacks/:stackId/alerting/rules/:ruleId` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-stack-alert-rule.md) for the provider-specific parameters and requirements.

