# RotaCloud: Get Clocked In User

Retrieves a clocked in user from RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-clocked-in-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-clocked-in-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/get-clocked-in-user?${params}`, {
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
| `id` | number | yes |  |

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

Through the native RotaCloud API, this operation is `GET /v1/users_clocked_in/:id` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-clocked-in-user.md) for the provider-specific parameters and requirements.

