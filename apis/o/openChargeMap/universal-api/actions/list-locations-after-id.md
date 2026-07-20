# Open Charge Map: List Locations After ID



```
GET https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-locations-after-id
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Open Charge Map `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-locations-after-id?connectionId=$CONNECTION_ID&greaterThanId=487000" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "greaterThanId": "487000"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/openChargeMap/latest/actions/list-locations-after-id?${params}`, {
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
| `greaterThanId` | string | yes | Return locations with an Open Charge Map POI ID greater than the provided value. Default: `487000`. Example: `487000`. |

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

Through the native Open Charge Map API, this operation is `GET /poi` (base URL `https://api.openchargemap.io/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations-after-id.md) for the provider-specific parameters and requirements.

