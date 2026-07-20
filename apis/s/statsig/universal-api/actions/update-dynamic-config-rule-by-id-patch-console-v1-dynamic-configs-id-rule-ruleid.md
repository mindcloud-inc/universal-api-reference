# Statsig: Update Dynamic Config Rule By Id

Updates a dynamic config rule in Statsig.

```
PUT https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-dynamic-config-rule-by-id-patch-console-v1-dynamic-configs-id-rule-ruleid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-dynamic-config-rule-by-id-patch-console-v1-dynamic-configs-id-rule-ruleid" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string",
  "ruleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/statsig/latest/actions/update-dynamic-config-rule-by-id-patch-console-v1-dynamic-configs-id-rule-ruleid', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string",
    "ruleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Dynamic Config ID |
| `ruleId` | string | yes | Rule ID |
| `name` | string | no | Request body field. |
| `passPercentage` | number | no | Request body field. |
| `conditions` | list | no | Request body field. |
| `environments` | list | no | Request body field. |
| `baseID` | string | no | Request body field. |
| `returnValue` | object | no | Request body field. |
| `completedAutomatedRollouts` | list | no | Request body field. |
| `pendingAutomatedRollouts` | list | no | Request body field. |
| `returnValueJson5` | string | no | Request body field. |
| `variants` | list | no | Request body field. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `dryRun` | boolean | no | Skips persisting updates to the entity (used to validate that inputs are correct) |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | Statsig response data payload. |
| `message` | string | Statsig response message. |

## Native endpoint

Through the native Statsig API, this operation is `PATCH /console/v1/dynamic_configs/{id}/rule/{ruleId}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-dynamic-config-rule-by-id-patch-console-v1-dynamic-configs-id-rule-ruleid.md) for the provider-specific parameters and requirements.

