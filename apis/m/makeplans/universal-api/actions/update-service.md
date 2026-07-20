# Makeplans: Update Service

Updates an existing service in Makeplans.

```
PUT https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-service
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Makeplans `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-service" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "serviceId": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/makeplans/latest/actions/update-service', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "serviceId": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `bookingType` | list | no | Service booking type. Use Attendance / Event when updating a service for events/classes. One of: `0`, `1`, `2`, `3`. |
| `interval` | number | no | Service interval in minutes. |
| `serviceId` | number | yes | The Makeplans service ID. |
| `title` | string | no | Service title. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": true,
      "booking_type": "string",
      "description": "string",
      "id": 1,
      "interval": 1,
      "price": 1,
      "title": "string",
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | boolean |  |
| `booking_type` | string |  |
| `description` | string |  |
| `id` | number |  |
| `interval` | number |  |
| `price` | number |  |
| `title` | string |  |
| `updated_at` | date |  |

## Native endpoint

Through the native Makeplans API, this operation is `PUT /services/:serviceId` (base URL `https://{{credentials.accountDomain}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-service.md) for the provider-specific parameters and requirements.

