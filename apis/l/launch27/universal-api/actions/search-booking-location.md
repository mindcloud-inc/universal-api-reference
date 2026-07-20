# Launch27: Search Booking Location

Finds a booking location in Launch27.

```
GET https://connect.mindcloud.co/v1/universal/launch27/latest/actions/search-booking-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Launch27 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/search-booking-location?connectionId=$CONNECTION_ID&address=string&zip=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "address": "string",
  "zip": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/search-booking-location?${params}`, {
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
| `address` | string | yes | Street address to search against Launch27 booking locations. |
| `zip` | string | yes | Postal code for the booking location search. |
| `city` | string | no | City for the booking location search. |
| `state` | string | no | State or region for the booking location search. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `name` | string |  |

## Native endpoint

Through the native Launch27 API, this operation is `POST booking/location` (base URL `https://{{credentials.subdomain}}.launch27.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-booking-location.md) for the provider-specific parameters and requirements.

