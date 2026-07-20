# RotaCloud: List Leave Types

Lists leave types in RotaCloud.

```
GET https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-types
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a RotaCloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-types?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/rotaCloud/latest/actions/list-leave-types?${params}`, {
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
      "can_request": true,
      "colour": "string",
      "id": 1,
      "name": "Ava Chen",
      "short_name": "Ava Chen",
      "time_attendance_only": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `can_request` | boolean |  |
| `colour` | string |  |
| `id` | number |  |
| `name` | string |  |
| `short_name` | string |  |
| `time_attendance_only` | boolean |  |

## Native endpoint

Through the native RotaCloud API, this operation is `GET /v1/leave_types` (base URL `https://api.rotacloud.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-leave-types.md) for the provider-specific parameters and requirements.

