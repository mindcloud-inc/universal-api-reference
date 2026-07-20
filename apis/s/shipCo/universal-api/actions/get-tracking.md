# Ship&Co: Get Tracking



```
GET https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/get-tracking
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ship&Co `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/get-tracking?connectionId=$CONNECTION_ID&carrier=string&trackingNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "carrier": "string",
  "trackingNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/shipCo/latest/actions/get-tracking?${params}`, {
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
| `carrier` | string | yes | Carrier code such as dhl, ups, fedex, japanpost, sagawa, yamato, or yuupack. |
| `trackingNumber` | string | yes | Carrier tracking number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "carrier": "string",
      "events": [
        {}
      ],
      "status": "string",
      "tracking_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `carrier` | string |  |
| `events` | array<object> |  |
| `status` | string |  |
| `tracking_number` | string |  |

## Native endpoint

Through the native Ship&Co API, this operation is `GET /tracking/:carrier/:trackingNumber` (base URL `https://api.shipandco.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-tracking.md) for the provider-specific parameters and requirements.

