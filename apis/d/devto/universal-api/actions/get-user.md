# Dev.to: Get User

Retrieves a Dev.to user by ID or username.

```
GET https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dev.to `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-user?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/devto/latest/actions/get-user?${params}`, {
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
| `id` | string | yes | User ID or username. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "id": 1,
      "location": "string",
      "name": "Ava Chen",
      "profile_image": "string",
      "summary": "string",
      "username": "Ava Chen",
      "website_url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `id` | number |  |
| `location` | string |  |
| `name` | string |  |
| `profile_image` | string |  |
| `summary` | string |  |
| `username` | string |  |
| `website_url` | string |  |

## Native endpoint

Through the native Dev.to API, this operation is `GET /users/:id` (base URL `https://dev.to/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

