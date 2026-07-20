# Grafana: Get Dashboard By UID

Retrieves a dashboard from Grafana by UID.

```
GET https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-dashboard-by-uid
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Grafana `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-dashboard-by-uid?connectionId=$CONNECTION_ID&uid=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "uid": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/grafana/latest/actions/get-dashboard-by-uid?${params}`, {
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
      "dashboard": {
        "id": 1,
        "title": "string",
        "uid": "string",
        "version": 1
      },
      "meta": {
        "folderTitle": "string",
        "folderUid": "string",
        "slug": "string",
        "url": "https://example.com",
        "version": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `dashboard.id` | number |  |
| `dashboard.title` | string |  |
| `dashboard.uid` | string |  |
| `dashboard.version` | number |  |
| `meta.folderTitle` | string |  |
| `meta.folderUid` | string |  |
| `meta.slug` | string |  |
| `meta.url` | string |  |
| `meta.version` | number |  |

## Native endpoint

Through the native Grafana API, this operation is `GET /dashboards/uid/:uid` (base URL `https://apps78aa.grafana.net/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-dashboard-by-uid.md) for the provider-specific parameters and requirements.

