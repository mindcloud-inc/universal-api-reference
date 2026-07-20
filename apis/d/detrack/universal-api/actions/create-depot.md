# Detrack: Create Depot

Creates a new depot in Detrack.

```
POST https://connect.mindcloud.co/v1/universal/detrack/latest/actions/create-depot
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Detrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/create-depot" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data.name": "Ava Chen",
  "data.address": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/detrack/latest/actions/create-depot', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data.name": "Ava Chen",
    "data.address": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `data.name` | string | yes | Depot name. |
| `data.address` | string | yes | Depot address that can be geocoded. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "addr1": {},
      "addr2": {},
      "addr3": {},
      "address": "string",
      "addressLat": 1,
      "addressLng": 1,
      "city": {},
      "country": {},
      "countryId": {},
      "id": "string",
      "location": [
        1
      ],
      "name": "Ava Chen",
      "state": {},
      "zipCode": {}
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `addr1` | object |  |
| `addr2` | object |  |
| `addr3` | object |  |
| `address` | string |  |
| `addressLat` | number |  |
| `addressLng` | number |  |
| `city` | object |  |
| `country` | object |  |
| `countryId` | object |  |
| `id` | string |  |
| `location[]` | number |  |
| `name` | string |  |
| `state` | object |  |
| `zipCode` | object |  |

## Native endpoint

Through the native Detrack API, this operation is `POST /dn/depots` (base URL `https://app.detrack.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-depot.md) for the provider-specific parameters and requirements.

