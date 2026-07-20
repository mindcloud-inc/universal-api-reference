# Deepset: Get Users

Retrieves users from your Deepset organization.

```
GET https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-users
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Deepset `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/deepset/latest/actions/get-users?${params}`, {
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
          "deleted": true,
          "email": "ava@example.com",
          "family_name": "Ava Chen",
          "given_name": "Ava Chen",
          "oauth_provider": "string",
          "organization": {
            "name": "Ava Chen",
            "organization_id": "string",
            "role": "string"
          },
          "user_id": "string"
        }
      ],
      "has_more": true,
      "total": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data[].deleted` | boolean |  |
| `data[].email` | string |  |
| `data[].family_name` | string |  |
| `data[].given_name` | string |  |
| `data[].oauth_provider` | string |  |
| `data[].organization.name` | string |  |
| `data[].organization.organization_id` | string |  |
| `data[].organization.role` | string |  |
| `data[].user_id` | string |  |
| `has_more` | boolean |  |
| `total` | number |  |

## Native endpoint

Through the native Deepset API, this operation is `GET /api/v1/users` (base URL `https://api.cloud.deepset.ai`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/get-users.md) for the provider-specific parameters and requirements.

