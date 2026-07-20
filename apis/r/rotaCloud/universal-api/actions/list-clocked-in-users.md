# RotaCloud: List Clocked In Users

Lists clocked in users in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-clocked-in-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-clocked-in-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-clocked-in-users?${params}`, {
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
      "breaks_clocked": [
        {}
      ],
      "in_device": "string",
      "in_location": {},
      "in_method": "string",
      "in_terminal": 1,
      "in_time": 1,
      "location": 1,
      "minutes_late": 1,
      "role": 1,
      "shift": 1,
      "user": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `breaks_clocked` | array<object> |  |
| `in_device` | string |  |
| `in_location` | object |  |
| `in_method` | string |  |
| `in_terminal` | number |  |
| `in_time` | number |  |
| `location` | number |  |
| `minutes_late` | number |  |
| `role` | number |  |
| `shift` | number |  |
| `user` | number |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/users_clocked_in` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-clocked-in-users.md) for the provider-specific parameters and requirements.

