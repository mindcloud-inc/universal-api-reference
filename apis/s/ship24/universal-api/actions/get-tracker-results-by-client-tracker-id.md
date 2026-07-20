# Ship24: Get Tracker Results By Client Tracker ID

Retrieves tracking results by client tracker ID in Ship24.

```
GET https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-client-tracker-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-client-tracker-id?connectionId=$CONNECTION_ID&trackerId=3fa99515-3ca0-4901-85bb-056ee016799b" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackerId": "3fa99515-3ca0-4901-85bb-056ee016799b"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-results-by-client-tracker-id?${params}`, {
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
| `trackerId` | string | yes | Your own client tracker ID value used to look up the tracker. Example: `3fa99515-3ca0-4901-85bb-056ee016799b`. |

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

Through the native Ship24 API, this operation is `GET /public/v1/trackers/:trackerId/results` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracker-results-by-client-tracker-id.md) for the provider-specific parameters and requirements.

