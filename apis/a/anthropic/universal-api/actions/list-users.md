# Anthropic: List Users

Retrieves users in the Anthropic organization.

```
GET https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Anthropic `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anthropic/latest/actions/list-users?${params}`, {
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
| `beforeId` | string | no | Cursor for previous page. |
| `afterId` | string | no | Cursor for next page. |
| `limit` | number | no | Number of records per page. |
| `email` | string | no | Filter users by email. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "data": [
        {}
      ],
      "firstId": "string",
      "hasMore": true,
      "lastId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data` | array<object> | List of users. |
| `firstId` | string | First user ID in the page. |
| `hasMore` | boolean | Whether more pages are available. |
| `lastId` | string | Last user ID in the page. |

## Native endpoint

Through the native Anthropic API, this operation is `GET /v1/organizations/users` (base URL `https://api.anthropic.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

