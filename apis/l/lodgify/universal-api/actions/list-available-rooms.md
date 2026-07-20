# Lodgify: List Available Rooms

Retrieves available room types from Lodgify.

```
GET https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-available-rooms
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Lodgify `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-available-rooms?connectionId=$CONNECTION_ID&id=779887" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "779887"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/lodgify/latest/actions/list-available-rooms?${params}`, {
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
| `id` | number | yes | Example: `779887`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "adultsOnly": true,
      "amenities": {},
      "area": 1,
      "areaUnit": "string",
      "bathrooms": 1,
      "bedrooms": 1,
      "breakfastIncluded": true,
      "description": "string",
      "hasMealPlan": true,
      "hasParking": true,
      "hasWifi": true,
      "id": 1,
      "images": [
        {}
      ],
      "imageUrl": "https://example.com",
      "maxPeople": 1,
      "maxPrice": 1,
      "minPrice": 1,
      "name": "Ava Chen",
      "originalMaxPrice": 1,
      "originalMinPrice": 1,
      "petsAllowed": true,
      "priceUnitInDays": 1,
      "showAdditionalKeyFacts": true,
      "units": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `adultsOnly` | boolean | Whether the room is adults only. |
| `amenities` | object | Grouped room amenities. |
| `area` | number | Room area value. |
| `areaUnit` | string | Area measurement unit. |
| `bathrooms` | number | Bathroom count. |
| `bedrooms` | number | Bedroom count. |
| `breakfastIncluded` | boolean | Whether breakfast is included. |
| `description` | string | Room description. |
| `hasMealPlan` | boolean | Whether a meal plan is available. |
| `hasParking` | boolean | Whether parking is available. |
| `hasWifi` | boolean | Whether Wi-Fi is available. |
| `id` | number | Room ID. |
| `images` | array<object> | Room image list. |
| `imageUrl` | string | Primary room image URL. |
| `maxPeople` | number | Maximum guest capacity. |
| `maxPrice` | number | Maximum price. |
| `minPrice` | number | Minimum price. |
| `name` | string | Room name. |
| `originalMaxPrice` | number | Original maximum price before discounts. |
| `originalMinPrice` | number | Original minimum price before discounts. |
| `petsAllowed` | boolean | Whether pets are allowed. |
| `priceUnitInDays` | number | Price unit duration in days. |
| `showAdditionalKeyFacts` | boolean | Whether extra key facts should be shown. |
| `units` | number | Number of units. |

## Native endpoint

Through the native Lodgify API, this operation is `GET /v2/properties/:id/rooms` (base URL `https://api.lodgify.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-available-rooms.md) for the provider-specific parameters and requirements.

