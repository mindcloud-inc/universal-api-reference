# Ship24: Get Tracker Results By Tracker ID

Retrieves tracking results for a Ship24 tracker ID.

```
GET https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-tracker-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-tracker-id?connectionId=$CONNECTION_ID&trackerId=26148317-7502-d3ac-44a9-546d240ac0dd" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackerId": "26148317-7502-d3ac-44a9-546d240ac0dd"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-tracker-id?${params}`, {
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
| `trackerId` | string | yes | Ship24 tracker ID returned when the tracker was created. Example: `26148317-7502-d3ac-44a9-546d240ac0dd`. |

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

Through the native Ship24 API, this operation is `GET /public/v1/trackers/:trackerId/results` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracker-results-by-tracker-id.md) for the provider-specific parameters and requirements.

