# NextBus: List Active Messages For Route

Retrieves active route messages from NextBus.

```
GET https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-active-messages-for-route
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-active-messages-for-route?connectionId=$CONNECTION_ID&agencyTag=stl&routeTag=252E" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agencyTag": "stl",
  "routeTag": "252E"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/list-active-messages-for-route?${params}`, {
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
| `agencyTag` | string | yes | Default: `stl`. |
| `routeTag` | string | yes | Default: `252E`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "message": [
        {}
      ],
      "tag": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `message` | array<object> |  |
| `tag` | string |  |

## Native endpoint

Through the native NextBus API, this operation is `GET /publicXMLFeed` (base URL `https://retro.umoiq.com/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-active-messages-for-route.md) for the provider-specific parameters and requirements.

