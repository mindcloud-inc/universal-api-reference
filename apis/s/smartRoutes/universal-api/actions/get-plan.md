# SmartRoutes: Get Plan



```
GET https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-plan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SmartRoutes `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-plan?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartRoutes/latest/actions/get-plan?${params}`, {
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
| `id` | number | yes | ID of the plan to retrieve. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "dispatched": true,
      "id": "string",
      "routes": [
        {}
      ],
      "totalTime": 1,
      "unserved": [
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
| `dispatched` | boolean | Whether the plan has been dispatched. |
| `id` | string | SmartRoutes plan identifier. |
| `routes` | array<object> | Routes attached to the plan. |
| `totalTime` | number | Total planned time returned by SmartRoutes. |
| `unserved` | array<object> | Unserved stops attached to the plan. |

## Native endpoint

Through the native SmartRoutes API, this operation is `GET /plans/:id` (base URL `https://api.smartroutes.io/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-plan.md) for the provider-specific parameters and requirements.

