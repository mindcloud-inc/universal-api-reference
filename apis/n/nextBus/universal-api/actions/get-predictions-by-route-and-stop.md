# NextBus: Get Predictions By Route And Stop

Retrieves stop predictions from NextBus by route and stop.

```
GET https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-predictions-by-route-and-stop
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-predictions-by-route-and-stop?connectionId=$CONNECTION_ID&agencyTag=glendale&routeTag=01&stopTag=gtc_d" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agencyTag": "glendale",
  "routeTag": "01",
  "stopTag": "gtc_d"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-predictions-by-route-and-stop?${params}`, {
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
| `agencyTag` | string | yes | Default: `glendale`. |
| `routeTag` | string | yes | Default: `01`. |
| `stopTag` | string | yes | Default: `gtc_d`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "agencyTitle": "string",
      "direction": [
        {}
      ],
      "routeTag": "string",
      "routeTitle": "string",
      "stopTag": "string",
      "stopTitle": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `agencyTitle` | string |  |
| `direction` | array<object> |  |
| `routeTag` | string |  |
| `routeTitle` | string |  |
| `stopTag` | string |  |
| `stopTitle` | string |  |

## Native endpoint

Through the native NextBus API, this operation is `GET /publicXMLFeed` (base URL `https://retro.umoiq.com/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-predictions-by-route-and-stop.md) for the provider-specific parameters and requirements.

