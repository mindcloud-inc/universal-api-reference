# Track-POD: Add Driver

Creates a new driver in Track-POD.

```
POST https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-driver
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Track-POD `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-driver" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/trackPOD/latest/actions/add-driver', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `Active` | boolean | no | Whether the driver is active. Default: `true`. |
| `Depot` | string | no | Depot name. |
| `DepotId` | string | no | Depot identifier. |
| `HomeAddress` | string | no | Driver home address. |
| `Name` | string | no | Driver name. |
| `Note` | string | no | Driver note. |
| `Password` | string | no | Driver password for Track-POD. |
| `Phone` | string | no | Driver phone number. |
| `Username` | string | no | Driver username for Track-POD. |
| `Vehicle` | string | no | Assigned vehicle number or name. |
| `Zone` | string | no | Driver zone. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "Detail": "string",
      "Status": 1,
      "Title": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `Detail` | string | A human-readable explanation specific to this response. |
| `Status` | number | The HTTP status code for the response |
| `Title` | string | A short, human-readable summary of the response |

## Native endpoint

Through the native Track-POD API, this operation is `POST /Driver` (base URL `https://api.track-pod.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/add-driver.md) for the provider-specific parameters and requirements.

