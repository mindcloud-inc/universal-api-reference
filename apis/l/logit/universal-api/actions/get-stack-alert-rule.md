# Logit: Get Stack Alert Rule

Retrieves a stack alert rule from Logit.

```
GET https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-alert-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-alert-rule?connectionId=$CONNECTION_ID&stackId=string&ruleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stackId": "string",
  "ruleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/logit/latest/actions/get-stack-alert-rule?${params}`, {
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

```json
{
  "success": true,
  "data": [
    {
      "configuration": "string",
      "createdAt": "string",
      "fileName": "Ava Chen",
      "isStale": true,
      "lastUpdated": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `configuration` | string |  |
| `createdAt` | string |  |
| `fileName` | string |  |
| `isStale` | boolean |  |
| `lastUpdated` | string |  |

## Native endpoint

Through the native Logit API, this operation is `GET /api/stacks/:stackId/alerting/rules/:ruleId` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stack-alert-rule.md) for the provider-specific parameters and requirements.

