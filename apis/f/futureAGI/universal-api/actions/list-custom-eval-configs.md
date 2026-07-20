# FutureAGI: List Custom Eval Configs



```
GET https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-custom-eval-configs
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a FutureAGI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-custom-eval-configs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/futureAGI/latest/actions/list-custom-eval-configs?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "result": [
        {
          "errorLocalizer": true,
          "evalTemplate": "string",
          "id": "string",
          "name": "Ava Chen",
          "project": "string"
        }
      ],
      "status": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `result` | array<object> |  |
| `result[].errorLocalizer` | boolean |  |
| `result[].evalTemplate` | string |  |
| `result[].id` | string |  |
| `result[].name` | string |  |
| `result[].project` | string |  |
| `status` | boolean |  |

## Native endpoint

Through the native FutureAGI API, this operation is `GET /tracer/custom-eval-config/list_custom_eval_configs/` (base URL `https://api.futureagi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-eval-configs.md) for the provider-specific parameters and requirements.

