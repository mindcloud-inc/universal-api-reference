# Datadog: List Dashboards

Retrieves dashboards from Datadog.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-dashboards
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-dashboards?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/list-dashboards?${params}`, {
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
| `filterShared` | boolean | no | Whether to return only shared dashboards. |
| `filterDeleted` | boolean | no | Whether to include deleted dashboards. |
| `count` | number | no | Maximum number of dashboards to return. |
| `start` | number | no | Starting offset for dashboard pagination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dashboards": [
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
| `dashboards` | array<object> | Dashboards returned by the list request. |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/dashboard` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-dashboards.md) for the provider-specific parameters and requirements.

