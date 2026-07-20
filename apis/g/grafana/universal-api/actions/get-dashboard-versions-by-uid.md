# Grafana: Get Dashboard Versions By UID

Retrieves dashboard versions from Grafana by UID.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-dashboard-versions-by-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-dashboard-versions-by-uid?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-dashboard-versions-by-uid?${params}`, {
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
| `uid` | string | yes | The dashboard UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created": "string",
      "dashboardId": 1,
      "id": 1,
      "message": "string",
      "uid": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created` | string |  |
| `dashboardId` | number |  |
| `id` | number |  |
| `message` | string |  |
| `uid` | string |  |
| `version` | number |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /dashboards/uid/:uid/versions` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard-versions-by-uid.md) for the provider-specific parameters and requirements.

