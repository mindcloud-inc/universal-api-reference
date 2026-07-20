# Logit: Create Stack Alert Rule

Creates a new stack alert rule in Logit.

```
POST https://connect.mindcloud.co/v1/universal/logit/latest/actions/create-stack-alert-rule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Logit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/logit/latest/actions/create-stack-alert-rule" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "stackId": "string",
  "newFileName": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/logit/latest/actions/create-stack-alert-rule', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "stackId": "string",
    "newFileName": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `stackId` | string | yes |  |
| `newFileName` | string | yes |  |
| `templateFileName` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "ruleId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `ruleId` | string |  |

## Native endpoint

Through the native Logit API, this operation is `POST /api/stacks/:stackId/alerting/rules` (base URL `https://dashboard.logit.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-stack-alert-rule.md) for the provider-specific parameters and requirements.

