# E2B: List Sandbox Metrics

Retrieves metrics for sandboxes from E2B.

```
GET https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandbox-metrics
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a E2B `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandbox-metrics?connectionId=$CONNECTION_ID&sandboxIds=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sandboxIds": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/e2B/latest/actions/list-sandbox-metrics?${params}`, {
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
| `sandboxIds` | string<string> | yes | Comma-separated list of sandbox IDs to get metrics for. Accepts multiple values in one string, delimited by `,`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "sandboxes": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `sandboxes` | object | Metrics keyed by sandbox ID. |

## Native endpoint

Through the native E2B API, this operation is `GET /sandboxes/metrics` (base URL `https://api.e2b.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-sandbox-metrics.md) for the provider-specific parameters and requirements.

