# Statsig: Delete Dynamic Config Rule

Deletes a dynamic config rule from Statsig.

```
DELETE https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-dynamic-config-rule-delete-console-v1-dynamic-configs-id-rule-ruleid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X DELETE "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-dynamic-config-rule-delete-console-v1-dynamic-configs-id-rule-ruleid?connectionId=$CONNECTION_ID&id=string&ruleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "ruleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/delete-dynamic-config-rule-delete-console-v1-dynamic-configs-id-rule-ruleid?${params}`, {
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
| `id` | string | yes | Dynamic Config ID |
| `ruleId` | string | yes | Rule ID |

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

Through the native Statsig API, this operation is `DELETE /console/v1/dynamic_configs/{id}/rule/{ruleId}` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/delete-dynamic-config-rule-delete-console-v1-dynamic-configs-id-rule-ruleid.md) for the provider-specific parameters and requirements.

