# Ship24: Create Tracker

Creates a new tracker in Ship24.

```
POST https://connect.mindcloud.co/v1/universal/ship24/latest/actions/create-tracker
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/create-tracker" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackingNumber": "9400115901047177598206"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ship24/latest/actions/create-tracker', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "trackingNumber": "9400115901047177598206"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `trackingNumber` | string | yes | Tracking number of the shipment. Example: `9400115901047177598206`. |
| `clientTrackerId` | string | no | Your unique identifier for this shipment. Example: `shipment-001`. |
| `shipmentReference` | string | no | Your reference for this shipment. Example: `ORD-10001`. |
| `originCountryCode` | string | no | Sender country code. Example: `CN`. |
| `destinationCountryCode` | string | no | Recipient country code. Recommended to improve tracking accuracy. Example: `US`. |
| `destinationPostCode` | string | no | Recipient postal or ZIP code. Recommended to improve tracking accuracy. Example: `94901`. |
| `shippingDate` | date | no | Shipment date. Keep it close to the real ship date to improve matching accuracy. Example: `2021-03-01T11:09:00.000Z`. |
| `courierCode[]` | array<string> | no | Up to 3 courier codes handling the shipment. Recommended to improve tracking accuracy. Example: `us-post`. |
| `courierName` | string | no | Courier name or service name. Example: `USPS Standard`. |
| `orderNumber` | string | no | Order number when the shipment comes from an ecommerce order. Example: `DF14R2022`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Example: `Nike shoes for Marc`. |
| `trackingUrl` | string | no | Example: `https://tools.usps.com/go/TrackConfirmAction?tLabels=9400115901047177598206`. |
| `recipient.name` | string | no | Example: `Marc`. |
| `recipient.email` | string | no | Example: `recipient@email.com`. |
| `settings.restrictTrackingToCourierCode` | boolean | no | If true, Ship24 only tracks the courier codes you provide. Default: `false`. |

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

Through the native Ship24 API, this operation is `POST /public/v1/trackers` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tracker.md) for the provider-specific parameters and requirements.

