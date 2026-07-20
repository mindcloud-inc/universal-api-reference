# Stackoverflow: List Users

Retrieves users from Stackoverflow.

```
GET https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Stackoverflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`), [sorting](../sorting.md) (`sort`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0&site=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0',
  "site": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/stackoverflow/latest/actions/list-users?${params}`, {
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
| `site` | string | yes | Stack Exchange site parameter, for example stackoverflow. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "account_id": 1,
      "creation_date": 1,
      "display_name": "Ava Chen",
      "last_access_date": 1,
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
| `account_id` | number |  |
| `creation_date` | number |  |
| `display_name` | string |  |
| `last_access_date` | number |  |
| `link` | string |  |
| `profile_image` | string |  |
| `reputation` | number |  |
| `user_id` | number |  |
| `user_type` | string |  |

## Native endpoint

Through the native Stackoverflow API, this operation is `GET /users` (base URL `https://api.stackexchange.com/2.3`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

