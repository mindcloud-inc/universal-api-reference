# Coast: Update Vehicle By ID



```
PUT https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatevehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatevehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "vehicleId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/updatevehicle', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "vehicleId": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `vehicleId` | string | yes | Coast vehicle ID of the vehicle to update. |
| `name` | string | no | Updated name for the vehicle. |
| `active` | boolean | no | Whether the vehicle is active in Coast. |
| `licensePlate` | string | no | Updated license plate for the vehicle. |
| `licensePlateState` | string | no | Updated license-plate state for the vehicle. |
| `make` | string | no | Updated make for the vehicle. |
| `model` | string | no | Updated model for the vehicle. |
| `modelYear` | string | no | Updated model year for the vehicle. |
| `vin` | string | no | Updated vehicle identification number. |
| `fuelType` | string | no | Updated fuel type for the vehicle. |
| `tankCapacity` | string | no | Updated tank capacity in hundredths of US gallons. |
| `departmentId` | string | no | Coast department ID to assign to the vehicle. |
| `locationId` | string | no | Coast location ID to assign to the vehicle. |
| `policyId` | string | no | Coast policy ID to assign to the vehicle. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coast API returns.

## Native endpoint

Through the native Coast API, this operation is `PATCH /v2/vehicles/:vehicleId` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/updatevehicle.md) for the provider-specific parameters and requirements.

