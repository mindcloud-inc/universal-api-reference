# Statsig: Read Dashboard Widget Results

Retrieves dashboard widget results from Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-dashboard-widget-results-get-console-v1-dashboards-id-widgets-widgetid-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

This action also supports [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-dashboard-widget-results-get-console-v1-dashboards-id-widgets-widgetid-results?connectionId=$CONNECTION_ID&id=string&widgetId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "widgetId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/read-dashboard-widget-results-get-console-v1-dashboards-id-widgets-widgetid-results?${params}`, {
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
| `id` | string | yes | dashboard id |
| `widgetId` | string | yes | widget id |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `samplingEnabled` | boolean | no | Whether funnel sampling should be enabled for this results query. Defaults to true. |

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

Through the native Statsig API, this operation is `GET /console/v1/dashboards/{id}/widgets/{widgetId}/results` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/read-dashboard-widget-results-get-console-v1-dashboards-id-widgets-widgetid-results.md) for the provider-specific parameters and requirements.

