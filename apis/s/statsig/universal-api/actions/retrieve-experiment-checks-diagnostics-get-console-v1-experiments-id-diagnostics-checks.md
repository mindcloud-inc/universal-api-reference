# Statsig: Retrieve Experiment Checks Diagnostics

Retrieves experiment checks diagnostics from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-experiment-checks-diagnostics-get-console-v1-experiments-id-diagnostics-checks
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-experiment-checks-diagnostics-get-console-v1-experiments-id-diagnostics-checks?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/retrieve-experiment-checks-diagnostics-get-console-v1-experiments-id-diagnostics-checks?${params}`, {
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
| `type` | string | no |  |
| `startDate` | string | no | Start date in YYYY-MM-DD format |
| `endDate` | string | no | End date in YYYY-MM-DD format |

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

Through the native Statsig API, this operation is `GET /console/v1/experiments/{id}/diagnostics_checks` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-experiment-checks-diagnostics-get-console-v1-experiments-id-diagnostics-checks.md) for the provider-specific parameters and requirements.

