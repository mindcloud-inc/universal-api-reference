# Ship24: Get Tracker By Client Tracker ID

Retrieves a tracker by client tracker ID from Ship24.

```
GET https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-by-client-tracker-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-by-client-tracker-id?connectionId=$CONNECTION_ID&trackerId=shipment-001" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackerId": "shipment-001"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracker-by-client-tracker-id?${params}`, {
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
| `trackerId` | string | yes | Example: `shipment-001`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "clientTrackerId": "string",
      "createdAt": "2026-05-07T12:00:00.000Z",
      "isSubscribed": true,
      "isTracked": true,
      "shipmentReference": "string",
      "trackerId": "string",
      "trackingNumber": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `clientTrackerId` | string | Client-defined tracker identifier. |
| `createdAt` | date | Tracker creation timestamp. |
| `isSubscribed` | boolean | Whether the tracker is active for webhook subscription. |
| `isTracked` | boolean | Whether Ship24 is still actively tracking this shipment. |
| `shipmentReference` | string | Shipment reference provided at tracker creation. |
| `trackerId` | string | Ship24 tracker identifier. |
| `trackingNumber` | string | Tracking number used for this tracker. |

## Native endpoint

Through the native Ship24 API, this operation is `GET /public/v1/trackers/:trackerId` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracker-by-client-tracker-id.md) for the provider-specific parameters and requirements.

