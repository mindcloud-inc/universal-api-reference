# Open Charge Map: Search Charging Locations



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/search-charging-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/search-charging-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/search-charging-locations?${params}`, {
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

Through the native Open Charge Map API, this operation is `GET /poi` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-charging-locations.md) for the provider-specific parameters and requirements.

