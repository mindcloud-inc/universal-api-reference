# Navigatr: Get User Detail

Retrieves user details from Navigatr.

```
GET https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/get-user-detail
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Navigatr `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/get-user-detail?connectionId=$CONNECTION_ID&userId=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "userId": "0"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/navigatr/latest/actions/get-user-detail?${params}`, {
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
| `userId` | number | yes | Default: `0`. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "avatar_url": "https://example.com",
      "bio": "string",
      "communities": [
        {
          "id": 1,
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "emails": [
        {
          "email": "ava@example.com",
          "is_primary": true,
          "is_verified": true,
          "user_id": 1
        }
      ],
      "firstname": "Ava",
      "id": 1,
      "interests": [
        "string"
      ],
      "lastname": "Chen",
      "learning_styles": [
        "string"
      ],
      "providers": [
        {
          "id": 1,
          "name": "Ava Chen",
          "url": "https://example.com"
        }
      ],
      "role": "string",
      "status": "string",
      "time_created": "2026-05-07T12:00:00.000Z",
      "time_updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `avatar_url` | string | Avatar URL |
| `bio` | string | User biography |
| `communities[].id` | number | Community ID |
| `communities[].name` | string | Community name |
| `communities[].url` | string | Community URL |
| `emails[].email` | string | Email address |
| `emails[].is_primary` | boolean | Whether the email is primary |
| `emails[].is_verified` | boolean | Whether the email is verified |
| `emails[].user_id` | number | Owning user ID |
| `firstname` | string | First name |
| `id` | number | User ID |
| `interests[]` | string | User interests |
| `lastname` | string | Last name |
| `learning_styles[]` | string | User learning styles |
| `providers[].id` | number | Provider ID |
| `providers[].name` | string | Provider name |
| `providers[].url` | string | Provider URL |
| `role` | string | User role |
| `status` | string | User status |
| `time_created` | date | Creation timestamp |
| `time_updated` | date | Last update timestamp |

## Native endpoint

Through the native Navigatr API, this operation is `GET /user_detail/:user_id` (base URL `https://api.navigatr.app/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-detail.md) for the provider-specific parameters and requirements.

