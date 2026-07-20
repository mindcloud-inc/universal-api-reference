# Stackoverflow: Get Authenticated User

Retrieves the authenticated user from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-authenticated-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-authenticated-user?connectionId=$CONNECTION_ID&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/get-authenticated-user?${params}`, {
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
| `site` | string | yes | The Stack Exchange site context to use when resolving the authenticated user, such as stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "accept_rate": 1,
      "account_id": 1,
      "display_name": "Ava Chen",
      "link": "https://example.com",
      "profile_image": "string",
      "reputation": 1,
      "user_id": 1,
      "user_type": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `accept_rate` | number |  |
| `account_id` | number |  |
| `display_name` | string |  |
| `link` | string |  |
| `profile_image` | string |  |
| `reputation` | number |  |
| `user_id` | number |  |
| `user_type` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /me` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-authenticated-user.md) for the provider-specific parameters and requirements.

