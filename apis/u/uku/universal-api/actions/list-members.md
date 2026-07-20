# Uku: List Members

Retrieves members from Uku.

```
GET https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-members
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Uku `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-members?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/uku/latest/actions/list-members?${params}`, {
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
      "address_city": "string",
      "address_country_code": "string",
      "avatar": "string",
      "avatar_fullsize": "string",
      "birthday": "string",
      "created_at": "string",
      "email": "ava@example.com",
      "group_ids": [
        1
      ],
      "id": 1,
      "initials": "string",
      "locale_code": "string",
      "name": "Ava Chen",
      "phone": "string",
      "region_code": "string",
      "status": "string",
      "surname": "Ava Chen",
      "timezone": "string",
      "updated_at": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `address_city` | string |  |
| `address_country_code` | string |  |
| `avatar` | string |  |
| `avatar_fullsize` | string |  |
| `birthday` | string |  |
| `created_at` | string |  |
| `email` | string |  |
| `group_ids` | array<number> |  |
| `id` | number |  |
| `initials` | string |  |
| `locale_code` | string |  |
| `name` | string |  |
| `phone` | string |  |
| `region_code` | string |  |
| `status` | string |  |
| `surname` | string |  |
| `timezone` | string |  |
| `updated_at` | string |  |

## Native endpoint

Through the native Uku API, this operation is `GET /members` (base URL `https://app.getuku.com/api/v1.0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-members.md) for the provider-specific parameters and requirements.

