# Statsig: Retrieve Experiment Summary Charts (Beta)

Retrieves experiment summary charts from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-experiment-summary-charts-beta-get-console-v1-experiments-id-summary-charts
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-experiment-summary-charts-beta-get-console-v1-experiments-id-summary-charts?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-experiment-summary-charts-beta-get-console-v1-experiments-id-summary-charts?${params}`, {
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
| `id` | string | yes | id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `control` | string | no | Optional override control group ID |
| `test` | string | no | Optional override test group ID. Use "*" to query against all test groups. |

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

Through the native Statsig API, this operation is `GET /console/v1/experiments/{id}/summary_charts` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-experiment-summary-charts-beta-get-console-v1-experiments-id-summary-charts.md) for the provider-specific parameters and requirements.

