# Ship24: Get Tracker Results By Tracking Number

Retrieves tracker results by tracking number in Ship24.

```
GET https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-tracking-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-tracking-number?connectionId=$CONNECTION_ID&trackingNumber=9400115901047177598206" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingNumber": "9400115901047177598206"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-tracking-number?${params}`, {
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
| `trackingNumber` | string | yes | Tracking number of the shipment. Example: `9400115901047177598206`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "events": [
        {}
      ],
      "shipment": {},
      "statistics": {},
      "tracker": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `events` | array<object> | Tracking events for the shipment. |
| `shipment` | object | Shipment summary returned by Ship24. |
| `statistics` | object | Shipment milestone timestamps and tracking statistics. |
| `tracker` | object | Tracker metadata for the tracked shipment. |

## Native endpoint

Through the native Ship24 API, this operation is `GET /public/v1/trackers/search/{trackingNumber}/results` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracker-results-by-tracking-number.md) for the provider-specific parameters and requirements.

