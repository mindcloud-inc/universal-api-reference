# Statsig: Get Dynamic Config or Experiment

Retrieves a dynamic config or experiment from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-dynamic-config-or-experiment-post-v1-get-config
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-dynamic-config-or-experiment-post-v1-get-config?connectionId=$CONNECTION_ID&configName=Ava%20Chen&user=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "configName": "Ava Chen",
  "user": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-dynamic-config-or-experiment-post-v1-get-config?${params}`, {
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
| `configName` | string | yes | Name of the dynamic config or experiment. |
| `user` | object | yes | Statsig user object containing at least one identifier. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `statsigMetadata` | object | no | SDK metadata for diagnostics and exposure behavior. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "group": "string",
      "group_name": "Ava Chen",
      "name": "Ava Chen",
      "rule_id": "string",
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `group` | string | Deprecated rule/group identifier. |
| `group_name` | string | Matched group name. |
| `name` | string | Config or experiment name. |
| `rule_id` | string | Matched rule ID. |
| `value` | object | Configuration values. |

## Native endpoint

Through the native Statsig API, this operation is `POST /v1/get_config` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dynamic-config-or-experiment-post-v1-get-config.md) for the provider-specific parameters and requirements.

