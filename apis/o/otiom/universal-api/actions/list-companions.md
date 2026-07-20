# Otiom: List Companions

Retrieves companions from Otiom.

```
GET https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-companions
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Otiom `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-companions?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/otiom/latest/actions/list-companions?${params}`, {
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
      "admin": {},
      "alarms": [
        "string"
      ],
      "avatar": "string",
      "email": "ava@example.com",
      "exit_advisory": [
        1
      ],
      "first_name": "Ava",
      "full_name": "Ava Chen",
      "id": 1,
      "last_name": "Chen",
      "mobile": "string",
      "patients": [
        "string"
      ],
      "profile_id": 1,
      "profile_type": "string",
      "registration_complete": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | object |  |
| `alarms` | array |  |
| `avatar` | string |  |
| `email` | string |  |
| `exit_advisory` | array<number> |  |
| `first_name` | string |  |
| `full_name` | string |  |
| `id` | number |  |
| `last_name` | string |  |
| `mobile` | string |  |
| `patients` | array |  |
| `profile_id` | number |  |
| `profile_type` | string |  |
| `registration_complete` | boolean |  |

## Native endpoint

Through the native Otiom API, this operation is `GET /api/companions/` (base URL `https://api.otiom.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-companions.md) for the provider-specific parameters and requirements.

