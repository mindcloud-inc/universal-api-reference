# Open Charge Map: List Charging Locations In Polygon



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-in-polygon
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-in-polygon?connectionId=$CONNECTION_ID&polygon=owweF~txjV%3Foe%60%40nnT%3F%3Fne%60%40" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "polygon": "owweF~txjV?oe`@nnT??ne`@"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-charging-locations-in-polygon?${params}`, {
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
| `polygon` | string | yes | Encoded polyline polygon shape. Open Charge Map automatically closes the polygon. Default: `owweF~txjV?oe`@nnT??ne`@`. Example: `owweF~txjV?oe`@nnT??ne`@`. |

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

Through the native Open Charge Map API, this operation is `GET /poi` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-charging-locations-in-polygon.md) for the provider-specific parameters and requirements.

