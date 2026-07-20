# Fleetio: Retrieve Meter Entry

Retrieves a specific meter entry from Fleetio.

```
GET https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-meter-entry
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Fleetio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-meter-entry?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fleetio/latest/actions/retrieve-meter-entry?${params}`, {
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
| `id` | string | yes | The id of the relevant record |

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
      "meterType": {},
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
| `meterType` | object |  |
| `type` | string |  |
| `updatedAt` | string |  |
| `value` | string |  |
| `vehicleId` | number |  |
| `void` | boolean |  |

## Native endpoint

Through the native Fleetio API, this operation is `GET meter_entries/:id` (base URL `https://secure.fleetio.com/api/`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-meter-entry.md) for the provider-specific parameters and requirements.

