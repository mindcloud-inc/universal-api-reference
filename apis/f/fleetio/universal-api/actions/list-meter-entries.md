# Fleetio: List Meter Entries

Retrieves a list of meter entries from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-meter-entries
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-meter-entries?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/list-meter-entries?${params}`, {
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
      "autoVoidedAt": {},
      "category": {},
      "createdAt": "string",
      "date": "string",
      "gpsProvider": "string",
      "id": 1,
      "meterableId": {},
      "meterableType": {},
      "meterType": "string",
      "type": "string",
      "updatedAt": "string",
      "value": "string",
      "vehicleId": 1,
      "void": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `autoVoidedAt` | object |  |
| `category` | object |  |
| `createdAt` | string |  |
| `date` | string |  |
| `gpsProvider` | string |  |
| `id` | number |  |
| `meterableId` | object |  |
| `meterableType` | object |  |
| `meterType` | string |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `value` | string |  |
| `vehicleId` | number |  |
| `void` | boolean |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET meter_entries` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-meter-entries.md) for the provider-specific parameters and requirements.

