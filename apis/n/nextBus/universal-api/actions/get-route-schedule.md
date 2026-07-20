# NextBus: Get Route Schedule

Retrieves a route schedule from NextBus.

```
GET https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-route-schedule
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-route-schedule?connectionId=$CONNECTION_ID&agencyTag=glendale&routeTag=01" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agencyTag": "glendale",
  "routeTag": "01"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-route-schedule?${params}`, {
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

## Response

```json
{
  "success": true,
  "data": [
    {
      "direction": "string",
      "header": {},
      "scheduleClass": "string",
      "serviceClass": "string",
      "tag": "string",
      "title": "string",
      "tr": [
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
| `direction` | string |  |
| `header` | object |  |
| `scheduleClass` | string |  |
| `serviceClass` | string |  |
| `tag` | string |  |
| `title` | string |  |
| `tr` | array<object> |  |

## Native endpoint

Through the native NextBus API, this operation is `GET /publicXMLFeed` (base URL `https://retro.umoiq.com/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-route-schedule.md) for the provider-specific parameters and requirements.

