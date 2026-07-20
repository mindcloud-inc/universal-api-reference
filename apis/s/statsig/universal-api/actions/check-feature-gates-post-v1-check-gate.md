# Statsig: Check Feature Gates

Checks feature gates in Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/check-feature-gates-post-v1-check-gate
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/check-feature-gates-post-v1-check-gate?connectionId=$CONNECTION_ID&gateName=Ava%20Chen&user=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "gateName": "Ava Chen",
  "user": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/check-feature-gates-post-v1-check-gate?${params}`, {
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
| `gateName` | string | yes | Single gate name to check. Use this or gateNames. |
| `user` | object | yes | Statsig user object containing at least one identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `gateNames` | list<string> | no | Array of gate names to check. Use this or gateName. |
| `statsigMetadata` | object | no | SDK metadata for diagnostics and exposure behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group_name": "Ava Chen",
      "name": "Ava Chen",
      "rule_id": "string",
      "value": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group_name` | string | Matched group name. |
| `name` | string | Gate name. |
| `rule_id` | string | Matched rule ID. |
| `value` | boolean | Whether the gate passes. |

## Native endpoint

Through the native Statsig API, this operation is `POST /v1/check_gate` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-feature-gates-post-v1-check-gate.md) for the provider-specific parameters and requirements.

