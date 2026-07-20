# MRPeasy: Get Routing

Retrieves a routing from MRPeasy.

```
GET https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-routing
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a MRPeasy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-routing?connectionId=$CONNECTION_ID&routingId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "routingId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mrpeasy/latest/actions/get-routing?${params}`, {
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
| `routingId` | number | yes | MRPeasy routing ID. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native MRPeasy API returns.

## Native endpoint

Through the native MRPeasy API, this operation is `GET /routings/{{routingId}}` (base URL `https://api.mrpeasy.com/rest/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-routing.md) for the provider-specific parameters and requirements.

