# Datadog: Get SLO History

Retrieves service level objective history from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-slo-history
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-slo-history?connectionId=$CONNECTION_ID&sloId=string&fromTs=1&toTs=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "sloId": "string",
  "fromTs": "1",
  "toTs": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/get-slo-history?${params}`, {
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
| `sloId` | string | yes | The ID of the service level objective. |
| `fromTs` | number | yes | Start of the history window in epoch seconds. |
| `toTs` | number | yes | End of the history window in epoch seconds. |
| `target` | number | no | Optional custom SLO target. |
| `applyCorrection` | boolean | no | Whether to apply SLO corrections. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": {},
      "errors": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | object | SLO history data returned by the request. |
| `errors` | array<object> | Errors returned while querying SLO history. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/slo/:slo_id/history` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-slo-history.md) for the provider-specific parameters and requirements.

