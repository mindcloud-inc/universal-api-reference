# Pinghome: List Service Heartbeats

Retrieves service heartbeats from Pinghome.

```
GET https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/list-service-heartbeats
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Pinghome `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/list-service-heartbeats?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/pinghome/latest/actions/list-service-heartbeats?${params}`, {
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
| `id` | string | yes | The unique ID of the service. |
| `page` | number | no | The page number to retrieve. |
| `limit` | number | no | The maximum number of heartbeats to return. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Pinghome API returns.

## Native endpoint

Through the native Pinghome API, this operation is `GET /resource-query/v1/service/:id/heartbeats` (base URL `https://api.pinghome.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-service-heartbeats.md) for the provider-specific parameters and requirements.

