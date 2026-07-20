# Coast: Create Vehicle



```
POST https://connect.mindcloud.co/v1/universal/coast/latest/actions/createvehicle
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Coast `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/coast/latest/actions/createvehicle" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "active": true
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/coast/latest/actions/createvehicle', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "active": true
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Friendly name for the vehicle. |
| `active` | boolean | yes | Whether the vehicle is active in Coast. |
| `licensePlate` | string | no | License plate for the vehicle. |
| `licensePlateState` | string | no | State associated with the vehicle license plate. |
| `make` | string | no | Vehicle make. |
| `model` | string | no | Vehicle model. |
| `modelYear` | string | no | Vehicle model year. |
| `vin` | string | no | Vehicle identification number. |
| `fuelType` | string | no | Vehicle fuel type. |
| `tankCapacity` | string | no | Tank capacity in hundredths of US gallons. |
| `departmentId` | string | no | Coast department ID to assign to the vehicle. |
| `locationId` | string | no | Coast location ID to assign to the vehicle. |
| `policyId` | string | no | Coast policy ID to assign to the vehicle. |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Coast API returns.

## Native endpoint

Through the native Coast API, this operation is `POST /v2/vehicles` (base URL `https://public.coastpay.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/createvehicle.md) for the provider-specific parameters and requirements.

