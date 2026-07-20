# Ship24: Create Tracker And Get Results

Creates a tracker and retrieves tracking results in Ship24.

```
POST https://connect.mindcloud.co/v1/universal/ship24/latest/actions/create-tracker-and-get-results
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/create-tracker-and-get-results" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "trackingNumber": "9400115901047177598206"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ship24/latest/actions/create-tracker-and-get-results', {
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
| `trackingNumber` | string | yes | Example: `9400115901047177598206`. |
| `clientTrackerId` | string | no | Example: `shipment-001`. |
| `shipmentReference` | string | no | Example: `ORD-10001`. |
| `originCountryCode` | string | no | Example: `CN`. |
| `destinationCountryCode` | string | no | Example: `US`. |
| `destinationPostCode` | string | no | Example: `94901`. |
| `shippingDate` | date | no | Example: `2021-03-01T11:09:00.000Z`. |
| `courierCode[]` | array<string> | no | Example: `us-post`. |
| `courierName` | string | no | Example: `USPS Standard`. |
| `orderNumber` | string | no | Example: `DF14R2022`. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `title` | string | no | Example: `Nike shoes for Marc`. |
| `trackingUrl` | string | no | Example: `https://tools.usps.com/go/TrackConfirmAction?tLabels=9400115901047177598206`. |
| `recipient.name` | string | no | Example: `Marc`. |
| `recipient.email` | string | no | Example: `recipient@email.com`. |
| `settings.restrictTrackingToCourierCode` | boolean | no | Default: `false`. |

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
| `events` | array<object> | Tracking events returned for the shipment. |
| `shipment` | object | Shipment summary returned by Ship24. |
| `statistics` | object | Shipment milestone timestamps and tracking statistics. |
| `tracker` | object | Tracker object returned by Ship24. |

## Native endpoint

Through the native Ship24 API, this operation is `POST /public/v1/trackers/track` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-tracker-and-get-results.md) for the provider-specific parameters and requirements.

