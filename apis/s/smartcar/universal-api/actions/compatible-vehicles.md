# Smartcar: Compatible Vehicles

Retrieves compatible vehicles from Smartcar.

```
GET https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/compatible-vehicles
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Smartcar `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/compatible-vehicles?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/smartcar/latest/actions/compatible-vehicles?${params}`, {
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
| `make` | string | no | Filter compatible vehicles by vehicle make. |
| `powertrainType` | string | no | Filter compatible vehicles by powertrain type. |
| `region` | string | no | Filter compatible vehicles by region. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "attributes": {},
      "id": "string",
      "type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `attributes` | object |  |
| `id` | string |  |
| `type` | string |  |

## Native endpoint

Through the native Smartcar API, this operation is `GET https://compatibility.api.smartcar.com/v3/compatible-vehicles` (base URL `https://vehicle.api.smartcar.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/compatible-vehicles.md) for the provider-specific parameters and requirements.

