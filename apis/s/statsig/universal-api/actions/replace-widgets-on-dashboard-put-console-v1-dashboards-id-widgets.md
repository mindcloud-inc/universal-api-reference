# Statsig: Replace Widgets on Dashboard

Replaces widgets on dashboard in Statsig.

```
GET https://connect.mindcloud.co/v1/universal/statsig/latest/actions/replace-widgets-on-dashboard-put-console-v1-dashboards-id-widgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Statsig `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/statsig/latest/actions/replace-widgets-on-dashboard-put-console-v1-dashboards-id-widgets?connectionId=$CONNECTION_ID&id=string&widgets=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string",
  "widgets": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/statsig/latest/actions/replace-widgets-on-dashboard-put-console-v1-dashboards-id-widgets?${params}`, {
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
| `widgets` | list | yes | Request body field. |
| `defaults` | object | no | Request body field. |
| `maxCols` | number | no | Request body field. |

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

Through the native Statsig API, this operation is `PUT /console/v1/dashboards/{id}/widgets` (base URL `https://statsigapi.net`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/replace-widgets-on-dashboard-put-console-v1-dashboards-id-widgets.md) for the provider-specific parameters and requirements.

