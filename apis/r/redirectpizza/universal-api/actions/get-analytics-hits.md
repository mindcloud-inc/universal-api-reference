# redirect.pizza: Get Analytics Hits



```
GET https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-hits
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a redirect.pizza `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-hits?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/redirectpizza/latest/actions/get-analytics-hits?${params}`, {
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
| `start` | string | no | Start date or timestamp for the analytics window. |
| `end` | string | no | End date or timestamp for the analytics window. |
| `query` | string | no | Filter expression for analytics results. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "count": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |

## Native endpoint

Through the native redirect.pizza API, this operation is `GET /api/v1/analytics/hits` (base URL `https://redirect.pizza`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-analytics-hits.md) for the provider-specific parameters and requirements.

