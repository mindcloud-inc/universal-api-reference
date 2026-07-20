# RotaCloud: List Leave Embargoes

Lists leave embargoes in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-embargoes
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-embargoes?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-embargoes?${params}`, {
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
      "end_am_pm": "string",
      "end_date": "string",
      "everyone": true,
      "id": 1,
      "message": "string",
      "start_am_pm": "string",
      "start_date": "string",
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
| `end_am_pm` | string |  |
| `end_date` | string |  |
| `everyone` | boolean |  |
| `id` | number |  |
| `message` | string |  |
| `start_am_pm` | string |  |
| `start_date` | string |  |
| `users` | array<number> |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/leave_embargoes` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leave-embargoes.md) for the provider-specific parameters and requirements.

