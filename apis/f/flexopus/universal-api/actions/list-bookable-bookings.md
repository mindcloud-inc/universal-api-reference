# Flexopus: List Bookable Bookings

Retrieves bookings for a specific Flexopus bookable.

```
GET https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-bookable-bookings
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-bookable-bookings?connectionId=$CONNECTION_ID&bookableId=1&from=2026-05-07T12%3A00%3A00.000Z&to=2026-05-07T12%3A00%3A00.000Z" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "bookableId": "1",
  "from": "2026-05-07T12:00:00.000Z",
  "to": "2026-05-07T12:00:00.000Z"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-bookable-bookings?${params}`, {
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
| `bookableId` | number | yes | The ID of the bookable resource. |
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
          "from": "2026-05-07T12:00:00.000Z",
          "guest": "string",
          "id": 1,
          "license_plate": "string",
          "livemap": "string",
          "to": "2026-05-07T12:00:00.000Z",
          "user": {
            "email": "ava@example.com",
            "extensionAttributes": {},
            "id": 1,
            "name": "Ava Chen"
          }
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
| `data[].from` | date |  |
| `data[].guest` | string |  |
| `data[].id` | number |  |
| `data[].license_plate` | string |  |
| `data[].livemap` | string |  |
| `data[].to` | date |  |
| `data[].user` | object |  |
| `data[].user.email` | string |  |
| `data[].user.extensionAttributes` | object |  |
| `data[].user.id` | number |  |
| `data[].user.name` | string |  |

## Native endpoint

Through the native Flexopus API, this operation is `GET /bookables/:bookable_id/bookings` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-bookable-bookings.md) for the provider-specific parameters and requirements.

