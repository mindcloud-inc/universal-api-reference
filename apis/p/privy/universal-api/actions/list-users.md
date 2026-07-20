# Privy: List Users

Retrieves a list of users from Privy.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/list-users?${params}`, {
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
      "data": [
        {
          "created_at": 1,
          "custom_metadata": {},
          "has_accepted_terms": true,
          "id": "string",
          "is_guest": true,
          "linked_accounts": [
            {
              "address": "https://example.com",
              "type": "https://example.com"
            }
          ]
        }
      ],
      "next_cursor": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].created_at` | number |  |
| `data[].custom_metadata` | object |  |
| `data[].has_accepted_terms` | boolean |  |
| `data[].id` | string |  |
| `data[].is_guest` | boolean |  |
| `data[].linked_accounts[].address` | string |  |
| `data[].linked_accounts[].type` | string |  |
| `next_cursor` | string |  |

## Native endpoint

Through the native Privy API, this operation is `GET /v1/users` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-users.md) for the provider-specific parameters and requirements.

