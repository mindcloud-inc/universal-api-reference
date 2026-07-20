# Loopy Loyalty: Update Location



```
PUT https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/update-location', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "id": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | Location ID. |
| `name` | string | no | Location name. |
| `lat` | number | no | Latitude. |
| `lon` | number | no | Longitude. |
| `address` | string | no | Human readable address of the location. |

### Advanced

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `alt` | number | no | Altitude. |
| `addressOnCard` | string | no | Human readable address, including organization name, for rendering on the card. |
| `message` | string | no | Message shown on the lock-screen when a customer is in the GPS range. |
| `showAddressOnCard` | boolean | no | Indicates if the address is shown on the card design. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "campaignsAffected": [
        "string"
      ],
      "location": {
        "address": "string",
        "id": "string",
        "lat": 1,
        "lon": 1,
        "name": "Ava Chen",
        "object": "string",
        "showAddressOnCard": true,
        "uid": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `campaignsAffected` | array<string> | Campaign IDs affected by the location update. |
| `location.address` | string | Human readable address. |
| `location.id` | string | Location ID. |
| `location.lat` | number | Latitude. |
| `location.lon` | number | Longitude. |
| `location.name` | string | Location name. |
| `location.object` | string | Resource type marker. |
| `location.showAddressOnCard` | boolean | Whether the address is shown on the card. |
| `location.uid` | string | Owner user ID. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `PATCH /location/:id` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/update-location.md) for the provider-specific parameters and requirements.

