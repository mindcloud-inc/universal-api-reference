# Open Charge Map: List Charging Locations In Bounding Box



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-in-bounding-box
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-in-bounding-box?connectionId=$CONNECTION_ID&boundingBox=(37.81%2C-122.52)%2C(37.70%2C-122.35)" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "boundingBox": "(37.81,-122.52),(37.70,-122.35)"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-in-bounding-box?${params}`, {
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
| `boundingBox` | string | yes | Bounding box as top-left and bottom-right corners: (lat,lng),(lat2,lng2). Default: `(37.81,-122.52),(37.70,-122.35)`. Example: `(37.81,-122.52),(37.70,-122.35)`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "AddressInfo": {},
      "Connections": [
        {}
      ],
      "DateLastStatusUpdate": "2026-05-07T12:00:00.000Z",
      "ID": 1,
      "OperatorInfo": {},
      "StatusType": {},
      "UUID": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `AddressInfo` | object |  |
| `Connections` | array<object> |  |
| `DateLastStatusUpdate` | date |  |
| `ID` | number |  |
| `OperatorInfo` | object |  |
| `StatusType` | object |  |
| `UUID` | string |  |

## Native endpoint

Through the native Open Charge Map API, this operation is `GET /poi` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-charging-locations-in-bounding-box.md) for the provider-specific parameters and requirements.

