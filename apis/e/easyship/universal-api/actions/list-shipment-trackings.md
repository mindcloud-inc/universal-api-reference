# Easyship: List Shipment Trackings

Retrieves shipment tracking history from Easyship.

```
GET https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipment-trackings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Easyship `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipment-trackings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyship/latest/actions/list-shipment-trackings?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "destinationCountryAlpha2": "string",
      "easyshipShipmentId": "string",
      "etaDate": "string",
      "originCountryAlpha2": "string",
      "platformOrderNumber": "string",
      "status": "string",
      "trackingPageUrl": "https://example.com",
      "trackings": [
        [
          {}
        ]
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `destinationCountryAlpha2` | string |  |
| `easyshipShipmentId` | string |  |
| `etaDate` | string |  |
| `originCountryAlpha2` | string |  |
| `platformOrderNumber` | string |  |
| `status` | string |  |
| `trackingPageUrl` | string |  |
| `trackings[]` | array<object> |  |

## Native endpoint

Through the native Easyship API, this operation is `GET /shipments/trackings` (base URL `https://public-api.easyship.com/2024-09`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-shipment-trackings.md) for the provider-specific parameters and requirements.

