# LimoExpress: List Vehicle Classes

Retrieves vehicle classes from the LimoExpress organization.

```
GET https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-vehicle-classes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a LimoExpress `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [filtering](../filtering.md) (`where`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-vehicle-classes?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/limoExpress/latest/actions/list-vehicle-classes?${params}`, {
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
| `searchString` | string | no | Search across vehicle class fields. |
| `page` | number | no | Page number, default is 1. |
| `perPage` | number | no | Items per page, default is 20. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "active": 1,
      "available_for_public": 1,
      "id": "string",
      "name": "Ava Chen",
      "number_of_passengers": 1,
      "number_of_suitcases": 1,
      "pictures": [
        "string"
      ],
      "price_per_hour": 1,
      "price_per_km": 1,
      "price_per_waiting_hour": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `active` | number | Active flag. |
| `available_for_public` | number | Public availability flag. |
| `id` | string | Vehicle class identifier. |
| `name` | string | Vehicle class name. |
| `number_of_passengers` | number | Passenger capacity. |
| `number_of_suitcases` | number | Suitcase capacity. |
| `pictures` | array<string> | Vehicle class image URLs. |
| `price_per_hour` | number | Price per hour. |
| `price_per_km` | number | Price per kilometer. |
| `price_per_waiting_hour` | number | Price per waiting hour. |

## Native endpoint

Through the native LimoExpress API, this operation is `GET /api/integration/vehicle-classes` (base URL `https://api.limoexpress.me`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-vehicle-classes.md) for the provider-specific parameters and requirements.

