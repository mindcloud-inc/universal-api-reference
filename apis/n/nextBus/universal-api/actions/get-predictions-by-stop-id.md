# NextBus: Get Predictions By Stop ID

Retrieves stop predictions from NextBus by stop ID.

```
GET https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-predictions-by-stop-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a NextBus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-predictions-by-stop-id?connectionId=$CONNECTION_ID&agencyTag=glendale&stopId=136" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "agencyTag": "glendale",
  "stopId": "136"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/nextBus/latest/actions/get-predictions-by-stop-id?${params}`, {
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
| `stopId` | string | yes | Default: `136`. |

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
      "dirTitleBecauseNoPredictions": "string",
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
| `dirTitleBecauseNoPredictions` | string |  |
| `routeTag` | string |  |
| `routeTitle` | string |  |
| `stopTag` | string |  |
| `stopTitle` | string |  |

## Native endpoint

Through the native NextBus API, this operation is `GET /publicXMLFeed` (base URL `https://retro.umoiq.com/service`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-predictions-by-stop-id.md) for the provider-specific parameters and requirements.

