# Flexopus: List User Bookings by Email

Retrieves bookings for a Flexopus user by email.

```
GET https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-user-bookings-by-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-user-bookings-by-email?connectionId=$CONNECTION_ID&userEmail=ava%40example.com&from=2026-05-07T12%3A00%3A00.000Z&to=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userEmail": "ava@example.com",
  "from": "2026-05-07T12:00:00.000Z",
  "to": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-user-bookings-by-email?${params}`, {
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
| `userEmail` | string | yes | The email address of the user. |
| `from` | date | yes | The start of the booking window as an ISO timestamp. |
| `to` | date | yes | The end of the booking window as an ISO timestamp. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "bookable": {
            "id": 1,
            "location": {
              "id": 1,
              "name": "Ava Chen"
            },
            "name": "Ava Chen",
            "status": 1,
            "type": 1
          },
          "from": "2026-05-07T12:00:00.000Z",
          "guest": "string",
          "id": 1,
          "license_plate": "string",
          "livemap": "string",
          "to": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> |  |
| `data[].bookable` | object |  |
| `data[].bookable.id` | number |  |
| `data[].bookable.location` | object |  |
| `data[].bookable.location.id` | number |  |
| `data[].bookable.location.name` | string |  |
| `data[].bookable.name` | string |  |
| `data[].bookable.status` | number |  |
| `data[].bookable.type` | number |  |
| `data[].from` | date |  |
| `data[].guest` | string |  |
| `data[].id` | number |  |
| `data[].license_plate` | string |  |
| `data[].livemap` | string |  |
| `data[].to` | date |  |

## Native endpoint

Through the native Flexopus API, this operation is `GET /users/by-email/:user_email/bookings` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-user-bookings-by-email.md) for the provider-specific parameters and requirements.

