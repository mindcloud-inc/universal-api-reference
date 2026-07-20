# Statsig: Retrieve Pulse Results

Retrieves pulse results from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-pulse-results-get-console-v1-gates-id-rules-ruleid-pulse-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-pulse-results-get-console-v1-gates-id-rules-ruleid-pulse-results?connectionId=$CONNECTION_ID&id=string&ruleID=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "ruleID": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-pulse-results-get-console-v1-gates-id-rules-ruleid-pulse-results?${params}`, {
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
| `id` | string | yes | Gate ID |
| `ruleID` | string | yes | Rule ID |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `cuped` | string | no | Whether to apply CUPED. Allowed values are "true" or "false". |
| `confidence` | string | no | Confidence interval (0-100) |

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

Through the native Statsig API, this operation is `GET /console/v1/gates/{id}/rules/{ruleID}/pulse_results` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-pulse-results-get-console-v1-gates-id-rules-ruleid-pulse-results.md) for the provider-specific parameters and requirements.

