# ThingsBoard: Get Time Series

Retrieves latest time series values from ThingsBoard.

```
GET https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-time-series
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a ThingsBoard `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-time-series?connectionId=$CONNECTION_ID&entityType=string&entityId=string&params=string&startTs=1&endTs=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "string",
  "entityId": "string",
  "params": "string",
  "startTs": "1",
  "endTs": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thingsBoard/latest/actions/get-time-series?${params}`, {
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
| `entityType` | string | yes | The ThingsBoard entity type, for example DEVICE. |
| `entityId` | string | yes | The ThingsBoard entity ID. |
| `params` | string | yes | Additional provider-specific telemetry query parameters. |
| `startTs` | number | yes | Start of the time range in Unix milliseconds. |
| `endTs` | number | yes | End of the time range in Unix milliseconds. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native ThingsBoard API returns.

## Native endpoint

Through the native ThingsBoard API, this operation is `GET /plugins/telemetry/:entityType/:entityId/values/timeseries` (base URL `{{credentials.baseUrl}}/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-time-series.md) for the provider-specific parameters and requirements.

