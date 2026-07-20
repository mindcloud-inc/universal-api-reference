# Thinkific: Get User

Retrieves a user record from Thinkific.

```
GET https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Thinkific `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/thinkific/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | Thinkific user ID or external ID when provider is supplied. |
| `provider` | string | no | Provider required when using an external user ID. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "administeredCourseIds": [
        1
      ],
      "createdAt": "string",
      "customProfileFields": [
        {}
      ],
      "email": "ava@example.com",
      "externalSource": "string",
      "firstName": "Ava",
      "fullName": "Ava Chen",
      "id": 1,
      "lastName": "Chen",
      "roles": [
        "string"
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `administeredCourseIds` | array<number> |  |
| `createdAt` | string |  |
| `customProfileFields` | array<object> |  |
| `email` | string |  |
| `externalSource` | string |  |
| `firstName` | string |  |
| `fullName` | string |  |
| `id` | number |  |
| `lastName` | string |  |
| `roles` | array<string> |  |

## Native endpoint

Through the native Thinkific API, this operation is `GET /users/:id` (base URL `https://api.thinkific.com/api/public/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

