# IntakeQ: Query Appointments

Retrieves appointments from IntakeQ.

```
GET https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a IntakeQ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/intakeQ/latest/actions/query-appointments?${params}`, {
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
      "bookedByClient": true,
      "clientDateOfBirth": "string",
      "clientEmail": "ava@example.com",
      "clientId": 1,
      "clientName": "Ava Chen",
      "clientPhone": "string",
      "createdBy": "string",
      "dateCreated": 1,
      "duration": 1,
      "endDate": 1,
      "externalClientId": "string",
      "id": "string",
      "intakeId": "string",
      "location": "string",
      "practitionerEmail": "ava@example.com",
      "practitionerName": "Ava Chen",
      "price": 1,
      "service": "string",
      "startDate": 1,
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `bookedByClient` | boolean |  |
| `clientDateOfBirth` | string |  |
| `clientEmail` | string |  |
| `clientId` | number |  |
| `clientName` | string |  |
| `clientPhone` | string |  |
| `createdBy` | string |  |
| `dateCreated` | number |  |
| `duration` | number |  |
| `endDate` | number |  |
| `externalClientId` | string |  |
| `id` | string |  |
| `intakeId` | string |  |
| `location` | string |  |
| `practitionerEmail` | string |  |
| `practitionerName` | string |  |
| `price` | number |  |
| `service` | string |  |
| `startDate` | number |  |
| `status` | string |  |

## Native endpoint

Through the native IntakeQ API, this operation is `GET /appointments` (base URL `https://intakeq.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/query-appointments.md) for the provider-specific parameters and requirements.

