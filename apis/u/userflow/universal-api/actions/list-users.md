# Userflow: List Users

Retrieves a list of users from Userflow.

```
GET https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-users?${params}`, {
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
| `limit` | number | no | Maximum number of users to return. |
| `startingAfter` | string | no | Return users after this user ID. |
| `orderBy` | string | no | Sort users by one or more supported fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "email": "ava@example.com",
            "name": "Ava Chen"
          },
          "created_at": "2026-05-07T12:00:00.000Z",
          "groups": {},
          "id": "string",
          "memberships": {},
          "object": "string"
        }
      ],
      "has_more": true,
      "next_page_url": "https://example.com",
      "object": "string",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of users. |
| `data[].attributes` | object | User attributes. |
| `data[].attributes.email` | string | User email. |
| `data[].attributes.name` | string | User name. |
| `data[].created_at` | date | User creation timestamp. |
| `data[].groups` | object | User groups. |
| `data[].id` | string | User ID. |
| `data[].memberships` | object | User memberships. |
| `data[].object` | string | Returned object type. |
| `has_more` | boolean | Whether more results are available. |
| `next_page_url` | string | URL for the next page. |
| `object` | string | Response object type. |
| `url` | string | Current page URL. |

## Native endpoint

Through the native Userflow API, this operation is `GET /users` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

