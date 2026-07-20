# Statsig: Get Ranked List for Contextual Bandit

Retrieves a ranked list from Statsig for contextual bandits.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-ranked-list-for-contextual-bandit-post-v1-get-ranked-list
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-ranked-list-for-contextual-bandit-post-v1-get-ranked-list?connectionId=$CONNECTION_ID&configName=Ava%20Chen&user=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "configName": "Ava Chen",
  "user": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/get-ranked-list-for-contextual-bandit-post-v1-get-ranked-list?${params}`, {
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
| `configName` | string | yes | Name of the contextual bandit/autotune experiment. |
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
      "name": "Ava Chen",
      "rule_id": "string",
      "score": 1,
      "value": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `name` | string | Variant name. |
| `rule_id` | string | Variant rule ID. |
| `score` | number | Predicted performance score. |
| `value` | object | Variant parameter values. |

## Native endpoint

Through the native Statsig API, this operation is `POST /v1/get_ranked_list` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-ranked-list-for-contextual-bandit-post-v1-get-ranked-list.md) for the provider-specific parameters and requirements.

