# GraphHopper: Calculate Route

Calculates a route between points in GraphHopper.

```
GET https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/calculate-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GraphHopper `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/calculate-route?connectionId=$CONNECTION_ID&requestBody=%5Bobject%20Object%5D" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "requestBody": "[object Object]"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/graphHopper/latest/actions/calculate-route?${params}`, {
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
| `requestBody` | object | yes | Route request JSON body matching GraphHopper's RouteRequest schema. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "hints": {},
      "info": {},
      "paths": [
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
| `hints` | object | Routing hints returned by GraphHopper. |
| `info` | object | Response metadata. |
| `paths` | array<object> | Calculated route paths. |

## Native endpoint

Through the native GraphHopper API, this operation is `POST /route` (base URL `https://graphhopper.com/api/1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/calculate-route.md) for the provider-specific parameters and requirements.

