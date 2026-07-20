# Flexopus: List Location Bookable Occupancy

Retrieves bookable occupancy for a Flexopus location.

```
GET https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-location-bookable-occupancy
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Flexopus `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-location-bookable-occupancy?connectionId=$CONNECTION_ID&locationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/flexopus/latest/actions/list-location-bookable-occupancy?${params}`, {
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
| `locationId` | number | yes | The ID of the location. |
| `details` | boolean | no | Include current and next booking details in the occupancy response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "id": "string",
          "location_name": "Ava Chen",
          "name": "Ava Chen",
          "occupied": true,
          "type": 1
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
| `data[].id` | string |  |
| `data[].location_name` | string |  |
| `data[].name` | string |  |
| `data[].occupied` | boolean |  |
| `data[].type` | number |  |

## Native endpoint

Through the native Flexopus API, this operation is `GET /locations/:location_id/bookables/occupancy` (base URL `{{credentials.tenantBaseUrl}}/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-location-bookable-occupancy.md) for the provider-specific parameters and requirements.

