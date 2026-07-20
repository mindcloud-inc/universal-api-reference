# SurveySparrow: Get User

Retrieves a user from SurveySparrow.

```
GET https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a SurveySparrow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-user?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/surveySparrow/latest/actions/get-user?${params}`, {
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
| `id` | number | yes | ID of the user |

## Response

```json
{
  "success": true,
  "data": [
    {
      "admin": true,
      "agency_owner": true,
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "id": 1,
      "name": "Ava Chen",
      "owner": true,
      "phone": "string",
      "role_id": 1,
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `admin` | boolean |  |
| `agency_owner` | boolean |  |
| `created_at` | date |  |
| `email` | string |  |
| `id` | number |  |
| `name` | string |  |
| `owner` | boolean |  |
| `phone` | string |  |
| `role_id` | number |  |
| `verified` | boolean |  |

## Native endpoint

Through the native SurveySparrow API, this operation is `GET /users/{{id}}` (base URL `https://api.surveysparrow.com/v3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

