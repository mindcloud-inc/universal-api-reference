# RotaCloud: List Locations

Lists locations in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-locations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-locations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-locations?${params}`, {
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
      "address": "string",
      "clock_in_ips": [
        "string"
      ],
      "deleted": true,
      "id": 1,
      "location": {},
      "managers": [
        1
      ],
      "metadata": {},
      "name": "Ava Chen",
      "timezone": 1,
      "users": [
        1
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address` | string |  |
| `clock_in_ips` | array<string> |  |
| `deleted` | boolean |  |
| `id` | number |  |
| `location` | object |  |
| `managers` | array<number> |  |
| `metadata` | object |  |
| `name` | string |  |
| `timezone` | number |  |
| `users` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/locations` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-locations.md) for the provider-specific parameters and requirements.

