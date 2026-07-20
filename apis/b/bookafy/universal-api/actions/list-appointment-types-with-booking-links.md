# Bookafy: List Appointment Types with Booking Links

Retrieves appointment types and booking links from Bookafy.

```
GET https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-appointment-types-with-booking-links
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Bookafy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-appointment-types-with-booking-links?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/bookafy/latest/actions/list-appointment-types-with-booking-links?${params}`, {
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
      "response": {
        "output": [
          {
            "assignedServices": [
              {
                "link": "https://example.com",
                "name": "Ava Chen"
              }
            ],
            "categories": [
              {
                "appointmentTypes": [
                  {
                    "link": "https://example.com",
                    "name": "Ava Chen"
                  }
                ],
                "link": "https://example.com",
                "name": "Ava Chen"
              }
            ],
            "client": 1
          }
        ]
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `response.output[].assignedServices[].link` | string | Booking link for the assigned service. |
| `response.output[].assignedServices[].name` | string | Assigned service name. |
| `response.output[].categories[].appointmentTypes[].link` | string | Booking link for the appointment type. |
| `response.output[].categories[].appointmentTypes[].name` | string | Appointment type name. |
| `response.output[].categories[].link` | string | Booking link for the category. |
| `response.output[].categories[].name` | string | Appointment type category name. |
| `response.output[].client` | number | Owning Bookafy client ID. |

## Native endpoint

Through the native Bookafy API, this operation is `GET /appointment_types` (base URL `https://app.bookafy.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointment-types-with-booking-links.md) for the provider-specific parameters and requirements.

