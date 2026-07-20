# Datadog: Search Monitors

Finds monitors in Datadog by query.

```
GET https://connect.mindcloud.co/v1/universal/datadog/latest/actions/search-monitors
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Datadog `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/datadog/latest/actions/search-monitors?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/datadog/latest/actions/search-monitors?${params}`, {
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
| `page` | number | no | Page number to start monitor search pagination from. |
| `perPage` | number | no | Number of monitor search results to return per page. |
| `query` | string | no | Monitor search query from the Datadog Manage Monitors page URL, for example type:metric status:alert. |
| `sort` | string | no | Sort order in the form field,direction such as name,asc or status,desc. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "counts": {},
      "metadata": {},
      "monitors": [
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
| `counts` | object |  |
| `metadata` | object |  |
| `monitors` | array<object> |  |

## Native endpoint

Through the native Datadog API, this operation is `GET /api/v1/monitor/search` (base URL `https://api.us5.datadoghq.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-monitors.md) for the provider-specific parameters and requirements.

