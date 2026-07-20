# Open Charge Map: Get Charging Location By ID



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-charging-location-by-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-charging-location-by-id?connectionId=$CONNECTION_ID&chargePointId=487642" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "chargePointId": "487642"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/get-charging-location-by-id?${params}`, {
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
| `chargePointId` | string | yes | Exact match on a given OCM POI ID. Comma-separated IDs are supported by Open Charge Map. Default: `487642`. Example: `487642`. |

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
| `AddressInfo` | object | Charging location address and coordinates. |
| `Connections` | array<object> | Available charging connections. |
| `DateLastStatusUpdate` | date | Last status update timestamp. |
| `ID` | number | Open Charge Map POI ID. |
| `OperatorInfo` | object | Charging location operator details. |
| `StatusType` | object | Operational status metadata. |
| `UUID` | string | Open Charge Map POI UUID. |

## Native endpoint

Through the native Open Charge Map API, this operation is `GET /poi` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-charging-location-by-id.md) for the provider-specific parameters and requirements.

