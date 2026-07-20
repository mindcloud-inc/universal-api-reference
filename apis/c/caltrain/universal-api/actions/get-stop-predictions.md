# Caltrain: Get Stop Predictions

Retrieves arrival predictions for a Caltrain stop.

```
GET https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-predictions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Caltrain `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-predictions?connectionId=$CONNECTION_ID&stopId=22nd_street" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "stopId": "22nd_street"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/caltrain/latest/actions/get-stop-predictions?${params}`, {
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
| `stopId` | string | yes | Caltrain parent stop identifier such as 22nd_street. Example: `22nd_street`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "meta": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `meta` | object |  |

## Native endpoint

Through the native Caltrain API, this operation is `GET /gtfs/stops/:stopId/predictions` (base URL `https://www.caltrain.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-stop-predictions.md) for the provider-specific parameters and requirements.

