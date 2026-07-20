# Privy: Search Users

Finds users in Privy by search term.

```
GET https://connect.mindcloud.co/v1/universal/privy/latest/actions/search-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Privy `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/privy/latest/actions/search-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/privy/latest/actions/search-users?${params}`, {
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
      ],
      "mfa_methods": [
        {
          "type": "string"
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
| `created_at` | number |  |
| `custom_metadata` | object |  |
| `has_accepted_terms` | boolean |  |
| `id` | string |  |
| `is_guest` | boolean |  |
| `linked_accounts[].address` | string |  |
| `linked_accounts[].type` | string |  |
| `mfa_methods[].type` | string |  |

## Native endpoint

Through the native Privy API, this operation is `POST /v1/users/search` (base URL `https://api.privy.io`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/search-users.md) for the provider-specific parameters and requirements.

