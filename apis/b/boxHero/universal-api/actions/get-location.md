# BoxHero: Get Location

Retrieves a location from BoxHero.

```
GET https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a BoxHero `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-location?connectionId=$CONNECTION_ID&locationId=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "locationId": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/boxHero/latest/actions/get-location?${params}`, {
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
| `locationId` | number | yes | Unique identifier for the location |

## Response

```json
{
  "success": true,
  "data": [
    {
      "item": {
        "id": 1,
        "memo": "string",
        "name": "Ava Chen",
        "quantity": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `item.id` | number |  |
| `item.memo` | string |  |
| `item.name` | string |  |
| `item.quantity` | number |  |

## Native endpoint

Through the native BoxHero API, this operation is `GET /v1/locations/:location_id` (base URL `https://rest.boxhero-app.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-location.md) for the provider-specific parameters and requirements.

