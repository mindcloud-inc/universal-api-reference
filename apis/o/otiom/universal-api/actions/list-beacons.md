# Otiom: List Beacons

Retrieves beacons from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-beacons
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-beacons?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-beacons?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": 1,
      "administrating": true,
      "battery_status": 1,
      "beacon_type": "string",
      "id": 1,
      "location": [
        1
      ],
      "mac_address": "string",
      "major": 1,
      "minor": 1,
      "name": "Ava Chen",
      "serial": "string",
      "site": 1,
      "user_given_name": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | number |  |
| `administrating` | boolean |  |
| `battery_status` | number |  |
| `beacon_type` | string |  |
| `id` | number |  |
| `location` | array<number> |  |
| `mac_address` | string |  |
| `major` | number |  |
| `minor` | number |  |
| `name` | string |  |
| `serial` | string |  |
| `site` | number |  |
| `user_given_name` | string |  |
| `uuid` | string |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/beacons/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-beacons.md) for the provider-specific parameters and requirements.

