# Solace PubSub+: Get Datacenter

Retrieves a datacenter from Solace PubSub+.

```
GET https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-datacenter
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Solace PubSub+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-datacenter?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/solacePubSub/latest/actions/get-datacenter?${params}`, {
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
| `id` | string | yes | Datacenter identifier. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "available": true,
      "datacenterType": "string",
      "id": "string",
      "location": {},
      "name": "Ava Chen",
      "operState": "string",
      "provider": "string",
      "type": "string",
      "visible": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `available` | boolean |  |
| `datacenterType` | string |  |
| `id` | string |  |
| `location` | object |  |
| `name` | string |  |
| `operState` | string |  |
| `provider` | string |  |
| `type` | string |  |
| `visible` | boolean |  |

## Native endpoint

Through the native Solace PubSub+ API, this operation is `GET /api/v2/missionControl/datacenters/{id}` (base URL `https://api.solace.cloud`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-datacenter.md) for the provider-specific parameters and requirements.

