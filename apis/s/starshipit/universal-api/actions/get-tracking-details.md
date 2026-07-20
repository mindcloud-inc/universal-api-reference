# Starshipit: Get Tracking Details



```
GET https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-tracking-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Starshipit `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-tracking-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/starshipit/latest/actions/get-tracking-details?${params}`, {
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
| `orderNumber` | string | no |  |
| `trackingNumber` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "results": {
        "carrierName": "Ava Chen",
        "carrierService": "string",
        "lastUpdatedDate": "2026-05-07T12:00:00.000Z",
        "orderNumber": "string",
        "orderStatus": "string",
        "shipmentDate": "2026-05-07T12:00:00.000Z",
        "trackingEvents": [
          {
            "details": "string",
            "eventDatetime": "2026-05-07T12:00:00.000Z",
            "status": "string"
          }
        ],
        "trackingNumber": "string",
        "trackingStatus": "string",
        "trackingUrl": "https://example.com"
      },
      "success": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `results` | object |  |
| `results.carrierName` | string |  |
| `results.carrierService` | string |  |
| `results.lastUpdatedDate` | date |  |
| `results.orderNumber` | string |  |
| `results.orderStatus` | string |  |
| `results.shipmentDate` | date |  |
| `results.trackingEvents` | array<object> |  |
| `results.trackingEvents[].details` | string |  |
| `results.trackingEvents[].eventDatetime` | date |  |
| `results.trackingEvents[].status` | string |  |
| `results.trackingNumber` | string |  |
| `results.trackingStatus` | string |  |
| `results.trackingUrl` | string |  |
| `success` | boolean |  |

## Native endpoint

Through the native Starshipit API, this operation is `GET /track` (base URL `https://api.starshipit.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracking-details.md) for the provider-specific parameters and requirements.

