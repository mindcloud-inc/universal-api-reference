# Instructure: Initiate Page Views Query

Initiates a page views query in Instructure Canvas.

```
POST https://connect.mindcloud.co/v1/universal/instructure/latest/actions/initiate-page-views-query
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Instructure `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/instructure/latest/actions/initiate-page-views-query" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "endDate": "string",
  "resultsFormat": "string",
  "startDate": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/instructure/latest/actions/initiate-page-views-query', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "endDate": "string",
    "resultsFormat": "string",
    "startDate": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `endDate` | string | yes | End date for the query. |
| `resultsFormat` | string | yes | Requested results format. |
| `startDate` | string | yes | Start date for the query. |

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

Through the native Instructure API, this operation is `POST /users/self/page_views/query` (base URL `https://canvas.instructure.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/initiate-page-views-query.md) for the provider-specific parameters and requirements.

