# SuperMCP: Get Async Query Results



```
GET https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-async-query-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SuperMCP `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-async-query-results?connectionId=$CONNECTION_ID&scheduleId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "scheduleId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/superMCP/latest/actions/get-async-query-results?${params}`, {
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
| `scheduleId` | string | yes | Opaque schedule_id returned by Query Marketing Data. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `compress` | boolean | no | Return a compact TOON response instead of JSON when supported. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | Returned query rows when ready. |
| `status` | string | Async query status. |

## Native endpoint

Through the native SuperMCP API, this operation is `POST /mcp/get_async_query_results` (base URL `https://mcp.supermetrics.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-async-query-results.md) for the provider-specific parameters and requirements.

