# Ziflow: List Users

Retrieves users from your Ziflow account.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-users?${params}`, {
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
      "count": 1,
      "has_more": true,
      "page": 1,
      "users": [
        {
          "account_owner": true,
          "accounts": [
            {
              "id": "string",
              "name": "Ava Chen",
              "primary": true
            }
          ],
          "active": true,
          "api_key": "string",
          "company": "string",
          "email": "ava@example.com",
          "first_name": "Ava",
          "group": [
            "string"
          ],
          "id": "string",
          "language": "string",
          "last_name": "Chen",
          "phone": "string",
          "proofing_defaults": {
            "comment": true,
            "decision": true,
            "manage": true,
            "notification": "string",
            "share": true
          },
          "roles": [
            "string"
          ],
          "timezone": "string",
          "verified": true
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `count` | number |  |
| `has_more` | boolean |  |
| `page` | number |  |
| `users[].account_owner` | boolean |  |
| `users[].accounts[].id` | string |  |
| `users[].accounts[].name` | string |  |
| `users[].accounts[].primary` | boolean |  |
| `users[].active` | boolean |  |
| `users[].api_key` | string |  |
| `users[].company` | string |  |
| `users[].email` | string |  |
| `users[].first_name` | string |  |
| `users[].group[]` | string |  |
| `users[].id` | string |  |
| `users[].language` | string |  |
| `users[].last_name` | string |  |
| `users[].phone` | string |  |
| `users[].proofing_defaults.comment` | boolean |  |
| `users[].proofing_defaults.decision` | boolean |  |
| `users[].proofing_defaults.manage` | boolean |  |
| `users[].proofing_defaults.notification` | string |  |
| `users[].proofing_defaults.share` | boolean |  |
| `users[].roles[]` | string |  |
| `users[].timezone` | string |  |
| `users[].verified` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /users` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

