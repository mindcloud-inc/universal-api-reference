# Shippify: Create Route

Creates delivery routes in Shippify asynchronously.

```
POST https://connect.mindcloud.co/v1/universal/shippify/latest/actions/create-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Shippify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/shippify/latest/actions/create-route" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "routes[]": [
    {}
  ],
  "iterations": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/shippify/latest/actions/create-route', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "routes[]": [{}],
    "iterations": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `routes[]` | array<object> | yes | Required array of route definitions. Each item follows Shippify's documented route object containing deliveries and route metadata. |
| `iterations` | number | yes | Required number of optimization iterations Shippify should run when creating the route. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": "string",
      "data": {
        "jobs": [
          [
            {}
          ]
        ],
        "routes": [
          [
            {}
          ]
        ]
      },
      "message": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | string | Shippify result code. |
| `data.jobs[]` | array<object> | Background route creation jobs. |
| `data.routes[]` | array<object> | Immediate route rows when returned by Shippify. |
| `message` | string | Shippify result message. |

## Native endpoint

Through the native Shippify API, this operation is `POST /v1/routes/create` (base URL `https://api.shippify.co`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-route.md) for the provider-specific parameters and requirements.

