# Samedi: List Upcoming Patient Appointments

Retrieves upcoming patient appointments from Samedi.

```
GET https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-upcoming-patient-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Samedi `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-upcoming-patient-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/samedi/latest/actions/list-upcoming-patient-appointments?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Samedi API returns.

## Native endpoint

Through the native Samedi API, this operation is `GET /booking/v3/events/upcoming` (base URL `https://patient.samedi.de/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-upcoming-patient-appointments.md) for the provider-specific parameters and requirements.

