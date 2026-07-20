# Cloutly: List Reviews

Retrieves reviews for connected sources in Cloutly.

```
GET https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-reviews
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Cloutly `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-reviews?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloutly/latest/actions/list-reviews?${params}`, {
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
| `businessId` | string | no | Filter reviews to one business. |
| `source` | string | no | Filter reviews by source. One of: `0`, `1`. |
| `showOnWidget` | boolean | no | Filter by widget visibility. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "reviews": [
        "string"
      ],
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `reviews` | array | Review records returned by Cloutly for the current page. |
| `total` | number | Total matching reviews available for the request. |

## Native endpoint

Through the native Cloutly API, this operation is `GET /reviews` (base URL `https://app.cloutly.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-reviews.md) for the provider-specific parameters and requirements.

