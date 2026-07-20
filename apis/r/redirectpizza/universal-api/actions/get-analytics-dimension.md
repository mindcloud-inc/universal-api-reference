# redirect.pizza: Get Analytics Dimension



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-dimension
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-dimension?connectionId=$CONNECTION_ID&limit=25&offset=0&dimension=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "dimension": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-dimension?${params}`, {
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
| `dimension` | string | yes | Analytics dimension to group by. |
| `start` | string | no | Start date or timestamp for the analytics window. |
| `end` | string | no | End date or timestamp for the analytics window. |
| `query` | string | no | Filter expression for analytics results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1,
      "key": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `key` | string |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `GET /api/v1/analytics/dimensions/{dimension}` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-analytics-dimension.md) for the provider-specific parameters and requirements.

