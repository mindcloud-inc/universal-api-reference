# Ship24: Get Tracking Results by Tracking Number

Retrieves tracking results by tracking number from Ship24.

```
GET https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracking-results-by-tracking-number
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship24 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracking-results-by-tracking-number?connectionId=$CONNECTION_ID&trackingNumber=9400115901047177598206" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "trackingNumber": "9400115901047177598206"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ship24/latest/actions/get-tracking-results-by-tracking-number?${params}`, {
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
      "shipment": {
        "delivery": {
          "courierEstimatedDeliveryDate": {},
          "estimatedDeliveryDate": {},
          "service": {},
          "signedBy": {}
        },
        "destinationCountryCode": {},
        "originCountryCode": {},
        "recipient": {
          "address": {},
          "city": {},
          "name": {},
          "postCode": {},
          "subdivision": {}
        },
        "shipmentId": {},
        "statusCategory": {},
        "statusCode": {},
        "statusMilestone": {},
        "trackingNumbers": [
          {
            "tn": "string"
          }
        ]
      },
      "statistics": {
        "timestamps": {
          "availableForPickupDatetime": {},
          "deliveredDatetime": {},
          "exceptionDatetime": {},
          "failedAttemptDatetime": {},
          "infoReceivedDatetime": {},
          "inTransitDatetime": {},
          "outForDeliveryDatetime": {}
        }
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `shipment.delivery.courierEstimatedDeliveryDate` | object |  |
| `shipment.delivery.estimatedDeliveryDate` | object |  |
| `shipment.delivery.service` | object |  |
| `shipment.delivery.signedBy` | object |  |
| `shipment.destinationCountryCode` | object |  |
| `shipment.originCountryCode` | object |  |
| `shipment.recipient.address` | object |  |
| `shipment.recipient.city` | object |  |
| `shipment.recipient.name` | object |  |
| `shipment.recipient.postCode` | object |  |
| `shipment.recipient.subdivision` | object |  |
| `shipment.shipmentId` | object |  |
| `shipment.statusCategory` | object |  |
| `shipment.statusCode` | object |  |
| `shipment.statusMilestone` | object |  |
| `shipment.trackingNumbers[].tn` | string |  |
| `statistics.timestamps.availableForPickupDatetime` | object |  |
| `statistics.timestamps.deliveredDatetime` | object |  |
| `statistics.timestamps.exceptionDatetime` | object |  |
| `statistics.timestamps.failedAttemptDatetime` | object |  |
| `statistics.timestamps.infoReceivedDatetime` | object |  |
| `statistics.timestamps.inTransitDatetime` | object |  |
| `statistics.timestamps.outForDeliveryDatetime` | object |  |

## Native endpoint

Through the native Ship24 API, this operation is `POST /public/v1/tracking/search` (base URL `https://api.ship24.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracking-results-by-tracking-number.md) for the provider-specific parameters and requirements.

