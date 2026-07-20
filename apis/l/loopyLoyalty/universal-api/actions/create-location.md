# Loopy Loyalty: Create Location



```
POST https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-location
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Loopy Loyalty `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-location" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "lat": 1,
  "lon": 1
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/loopyLoyalty/latest/actions/create-location', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "lat": 1,
    "lon": 1
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `name` | string | yes | Location name. |
| `lat` | number | yes | Latitude. |
| `lon` | number | yes | Longitude. |
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
      "id": "string",
      "newLocation": {
        "address": "string",
        "id": "string",
        "lat": 1,
        "lon": 1,
        "name": "Ava Chen",
        "object": "string",
        "showAddressOnCard": true,
        "uid": "string"
      },
      "revision": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | string | Created location ID. |
| `newLocation.address` | string | Human readable address. |
| `newLocation.id` | string | Location ID. |
| `newLocation.lat` | number | Latitude. |
| `newLocation.lon` | number | Longitude. |
| `newLocation.name` | string | Location name. |
| `newLocation.object` | string | Resource type marker. |
| `newLocation.showAddressOnCard` | boolean | Whether the address is shown on the card. |
| `newLocation.uid` | string | Owner user ID. |
| `revision` | string | Revision token returned by Loopy Loyalty. |

## Native endpoint

Through the native Loopy Loyalty API, this operation is `POST /location` (base URL `https://api.loopyloyalty.com/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-location.md) for the provider-specific parameters and requirements.

