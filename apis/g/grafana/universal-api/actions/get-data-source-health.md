# Grafana: Get Data Source Health

Retrieves data source health from Grafana.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-data-source-health
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-data-source-health?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-data-source-health?${params}`, {
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
| `uid` | string | yes | The data source UID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "details": {
        "application": "string",
        "features": {
          "rulerApiEnabled": true
        }
      },
      "message": "string",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `details.application` | string |  |
| `details.features.rulerApiEnabled` | boolean |  |
| `message` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /datasources/uid/:uid/health` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-data-source-health.md) for the provider-specific parameters and requirements.

