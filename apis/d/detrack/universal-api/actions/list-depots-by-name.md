# Detrack: List Depots By Name

Finds depots in Detrack by depot name.

```
GET https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-depots-by-name
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Detrack `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-depots-by-name?connectionId=$CONNECTION_ID&name=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "name": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/detrack/latest/actions/list-depots-by-name?${params}`, {
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
| `name` | string | yes | Depot name. |

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

Through the native Detrack API, this operation is `GET /dn/depots` (base URL `https://app.detrack.com/api/v2`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-depots-by-name.md) for the provider-specific parameters and requirements.

