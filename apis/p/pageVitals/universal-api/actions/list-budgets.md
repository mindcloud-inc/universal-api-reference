# PageVitals: List Budgets



```
GET https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-budgets
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a PageVitals `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-budgets?connectionId=$CONNECTION_ID&websiteId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "websiteId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pageVitals/latest/actions/list-budgets?${params}`, {
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
| `websiteId` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "device": "string",
      "id": "string",
      "metric": "string",
      "operator": "string",
      "pages": [
        {}
      ],
      "status": "string",
      "value": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `device` | string |  |
| `id` | string |  |
| `metric` | string |  |
| `operator` | string |  |
| `pages` | array<object> |  |
| `status` | string |  |
| `value` | number |  |

## Native endpoint

Through the native PageVitals API, this operation is `GET /:websiteId/budgets` (base URL `https://api.pagevitals.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-budgets.md) for the provider-specific parameters and requirements.

