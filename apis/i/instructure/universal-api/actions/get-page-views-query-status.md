# Instructure: Get Page Views Query Status

Retrieves page views query status from Instructure Canvas.

```
GET https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-page-views-query-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-page-views-query-status?connectionId=$CONNECTION_ID&queryId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "queryId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/instructure/latest/actions/get-page-views-query-status?${params}`, {
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
| `queryId` | string | yes | Page views query ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "poll_url": "https://example.com",
      "query_id": "string",
      "results_url": "https://example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `poll_url` | string |  |
| `query_id` | string |  |
| `results_url` | string |  |
| `status` | string |  |

## Native endpoint

Through the native Instructure API, this operation is `GET /users/self/page_views/query/:query_id` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-page-views-query-status.md) for the provider-specific parameters and requirements.

