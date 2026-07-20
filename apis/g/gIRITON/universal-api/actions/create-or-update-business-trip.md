# GIRITON: Create Or Update Business Trip

Creates or updates a business trip in GIRITON.

```
PUT https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/create-or-update-business-trip
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a GIRITON `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/create-or-update-business-trip" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "person.id": "string",
  "dateTimeFrom": "2026-04-30T09:00+02:00",
  "dateTimeTo": "2026-04-30T17:00+02:00"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/gIRITON/latest/actions/create-or-update-business-trip', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "person.id": "string",
    "dateTimeFrom": "2026-04-30T09:00+02:00",
    "dateTimeTo": "2026-04-30T17:00+02:00"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `person.id` | string | yes | Person ID nested under the GIRITON person request object. |
| `dateTimeFrom` | string | yes | Business trip start date and time in GIRITON's documented ISO offset format. Example: `2026-04-30T09:00+02:00`. |
| `dateTimeTo` | string | yes | Business trip end date and time in GIRITON's documented ISO offset format. Example: `2026-04-30T17:00+02:00`. |
| `description` | string | no | Business trip description. |
| `distanceKm` | number | no | Business trip distance in kilometers. |
| `foreignTrip` | boolean | no | Whether the business trip is foreign. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "customFieldId1": "string",
      "customFieldId2": 1,
      "customFieldId3": true,
      "dateTimeFrom": "string",
      "dateTimeTo": "string",
      "description": "string",
      "distanceKm": 1,
      "entryTimestamp": "2026-05-07T12:00:00.000Z",
      "foreignTrip": true,
      "id": "string",
      "person": {},
      "placeFrom": "string",
      "placeTo": "string",
      "refuellingRecords": [
        {}
      ],
      "vehicleLicencePlate": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `customFieldId1` | string | Custom field value. |
| `customFieldId2` | number | Custom field value. |
| `customFieldId3` | boolean | Custom field value. |
| `dateTimeFrom` | string | Business trip start date and time. |
| `dateTimeTo` | string | Business trip end date and time. |
| `description` | string | Business trip description. |
| `distanceKm` | number | Business trip distance in kilometers. |
| `entryTimestamp` | date | Business trip entry timestamp. |
| `foreignTrip` | boolean | Whether the trip is foreign. |
| `id` | string | Business trip ID. |
| `person` | object | Person details. |
| `placeFrom` | string | Start place. |
| `placeTo` | string | Destination place. |
| `refuellingRecords` | array<object> | Refuelling records. |
| `vehicleLicencePlate` | string | Vehicle licence plate. |

## Native endpoint

Through the native GIRITON API, this operation is `POST /attendance/businessTrip` (base URL `https://rest.giriton.com/system/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-or-update-business-trip.md) for the provider-specific parameters and requirements.

