# Ship24: Update Tracker

Updates an existing tracker in Ship24.

```
PUT https://connect.mindcloud.co/v1/universal/ship24/latest/actions/update-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/update-tracker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackerId": "26148317-7502-d3ac-44a9-546d240ac0dd"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ship24/latest/actions/update-tracker', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackerId": "26148317-7502-d3ac-44a9-546d240ac0dd"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackerId` | string | yes | Ship24 tracker ID returned when the tracker was created. Example: `26148317-7502-d3ac-44a9-546d240ac0dd`. |
| `isSubscribed` | boolean | no | Set false to stop future tracking updates and webhook notifications. Example: `true`. |
| `originCountryCode` | string | no | Sender country code in ISO alpha-2 or alpha-3 format. Example: `CN`. |
| `destinationCountryCode` | string | no | Recipient country code in ISO alpha-2 or alpha-3 format. Example: `US`. |
| `destinationPostCode` | string | no | Recipient postal code or ZIP code. Example: `94901`. |
| `shippingDate` | date | no | Shipment date in an ISO-compatible date or datetime format. Example: `2021-03-01`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `courierCode` | string | no | Courier code that handles the shipment. Ship24 allows up to 3 codes. Example: `us-post`. |

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

Through the native Ship24 API, this operation is `PATCH /public/v1/trackers/:trackerId` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-tracker.md) for the provider-specific parameters and requirements.

