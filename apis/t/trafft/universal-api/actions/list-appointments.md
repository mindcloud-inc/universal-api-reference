# Trafft: List Appointments

Retrieves appointments from Trafft.

```
GET https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-appointments
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Trafft `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-appointments?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/trafft/latest/actions/list-appointments?${params}`, {
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
      "data": {
        "bookings": {
          "additional_persons": 1,
          "customer": {
            "email": "ava@example.com",
            "first_name": "Ava",
            "id": 1,
            "last_name": "Chen"
          },
          "id": 1,
          "status": "string"
        },
        "created_at": "string",
        "employees": {
          "first_name": "Ava",
          "id": 1,
          "last_name": "Chen"
        },
        "end_date_time": "string",
        "id": 1,
        "location": {},
        "note": "string",
        "service": {
          "id": 1,
          "name": "Ava Chen"
        },
        "start_date_time": "string",
        "status": "string"
      },
      "pagination": {
        "limit": 1,
        "page": 1,
        "pages": 1,
        "total": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data.bookings` | array<object> |  |
| `data.bookings.additional_persons` | number |  |
| `data.bookings.customer` | object |  |
| `data.bookings.customer.email` | string |  |
| `data.bookings.customer.first_name` | string |  |
| `data.bookings.customer.id` | number |  |
| `data.bookings.customer.last_name` | string |  |
| `data.bookings.id` | number |  |
| `data.bookings.status` | string |  |
| `data.created_at` | string |  |
| `data.employees` | array<object> |  |
| `data.employees.first_name` | string |  |
| `data.employees.id` | number |  |
| `data.employees.last_name` | string |  |
| `data.end_date_time` | string |  |
| `data.id` | number |  |
| `data.location` | object |  |
| `data.note` | string |  |
| `data.service` | object |  |
| `data.service.id` | number |  |
| `data.service.name` | string |  |
| `data.start_date_time` | string |  |
| `data.status` | string |  |
| `pagination` | object |  |
| `pagination.limit` | number |  |
| `pagination.page` | number |  |
| `pagination.pages` | number |  |
| `pagination.total` | number |  |

## Native endpoint

Through the native Trafft API, this operation is `GET /appointments` (base URL `https://mindcloud.admin.trafft.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-appointments.md) for the provider-specific parameters and requirements.

