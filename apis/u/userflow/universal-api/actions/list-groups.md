# Userflow: List Groups

Retrieves a list of groups from Userflow.

```
GET https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Userflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/userflow/latest/actions/list-groups?${params}`, {
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
| `limit` | number | no | Maximum number of groups to return. |
| `startingAfter` | string | no | Return groups after this group ID. |
| `orderBy` | string | no | Sort groups by one or more supported fields. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {
          "attributes": {
            "name": "Ava Chen"
          },
          "created_at": "2026-05-07T12:00:00.000Z",
          "id": "string",
          "memberships": {},
          "object": "string",
          "users": {}
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
| `data` | array<object> | List of groups. |
| `data[].attributes` | object | Group attributes. |
| `data[].attributes.name` | string | Group name. |
| `data[].created_at` | date | Group creation timestamp. |
| `data[].id` | string | Group ID. |
| `data[].memberships` | object | Group memberships. |
| `data[].object` | string | Returned object type. |
| `data[].users` | object | Users in the group. |
| `has_more` | boolean | Whether more results are available. |
| `next_page_url` | string | URL for the next page. |
| `object` | string | Response object type. |
| `url` | string | Current page URL. |

## Native endpoint

Through the native Userflow API, this operation is `GET /groups` (base URL `https://api.userflow.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-groups.md) for the provider-specific parameters and requirements.

