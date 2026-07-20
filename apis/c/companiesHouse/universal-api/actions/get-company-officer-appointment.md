# Companies House: Get Company Officer Appointment

Retrieves a company officer appointment from Companies House.

```
GET https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-officer-appointment
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Companies House `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-officer-appointment?connectionId=$CONNECTION_ID&appointmentId=string&companyNumber=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "appointmentId": "string",
  "companyNumber": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/companiesHouse/latest/actions/get-company-officer-appointment?${params}`, {
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
| `appointmentId` | string | yes | The appointment ID. |
| `companyNumber` | string | yes | The company number. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "appointed_on": "string",
      "etag": "string",
      "is_pre_1992_appointment": true,
      "links": {},
      "name": "Ava Chen",
      "officer_role": "string",
      "person_number": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `appointed_on` | string |  |
| `etag` | string |  |
| `is_pre_1992_appointment` | boolean |  |
| `links` | object |  |
| `name` | string |  |
| `officer_role` | string |  |
| `person_number` | string |  |

## Native endpoint

Through the native Companies House API, this operation is `GET /company/:company_number/appointments/:appointment_id` (base URL `https://api.company-information.service.gov.uk`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-company-officer-appointment.md) for the provider-specific parameters and requirements.

