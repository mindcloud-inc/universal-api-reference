# Onfleet: Create Destination

Creates a new destination in Onfleet.

```
POST https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-destination
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Onfleet `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-destination" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "address.number": "string",
  "address.street": "string",
  "address.city": "string",
  "address.country": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onfleet/latest/actions/create-destination', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "address.number": "string",
    "address.street": "string",
    "address.city": "string",
    "address.country": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `address.number` | string | yes | The number component of the destination address. |
| `address.street` | string | yes | The street component of the destination address. |
| `address.city` | string | yes | The city component of the destination address. |
| `address.country` | string | yes | The country component of the destination address. |
| `address.name` | string | no | Optional name associated with this address. |
| `address.apartment` | string | no | Optional apartment or suite information. |
| `address.state` | string | no | Optional state or province information. |
| `address.postalCode` | string | no | Optional postal or zip code. |
| `address.unparsed` | string | no | Optional complete address string to geocode. |
| `notes` | string | no | Optional notes about the destination. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "address": {},
      "id": "string",
      "location": [
        1
      ],
      "notes": "string",
      "useGPS": true,
      "warnings": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | object |  |
| `id` | string |  |
| `location` | array<number> |  |
| `notes` | string |  |
| `useGPS` | boolean |  |
| `warnings` | array<string> |  |

## Native endpoint

Through the native Onfleet API, this operation is `POST /destinations` (base URL `https://onfleet.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-destination.md) for the provider-specific parameters and requirements.

