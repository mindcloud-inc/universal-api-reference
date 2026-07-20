# Sunwise: Search Reports

Finds reports in Sunwise by search term.

```
GET https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/search-reports
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Sunwise `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/search-reports?connectionId=$CONNECTION_ID&query=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "query": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sunwise/latest/actions/search-reports?${params}`, {
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
| `query` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "string",
      "id": "string",
      "name": "Ava Chen",
      "status": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | string |  |
| `id` | string |  |
| `name` | string |  |
| `status` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Sunwise API, this operation is `GET /reports/report-search/` (base URL `https://production.sunwise.ai/boty/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-reports.md) for the provider-specific parameters and requirements.

