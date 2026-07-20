# Monica CRM: Get Me

Retrieves your user profile from Monica CRM.

```
GET https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-me
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Monica CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-me?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/monicaCRM/latest/actions/get-me?${params}`, {
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
      "data": {
        "account": {
          "id": 1
        },
        "created_at": "string",
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": 1,
        "is_policy_compliant": true,
        "last_name": "Chen",
        "locale": "string",
        "name": "Ava Chen",
        "object": "string",
        "timezone": "string",
        "updated_at": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `data.account.id` | number |  |
| `data.created_at` | string |  |
| `data.email` | string |  |
| `data.first_name` | string |  |
| `data.id` | number |  |
| `data.is_policy_compliant` | boolean |  |
| `data.last_name` | string |  |
| `data.locale` | string |  |
| `data.name` | string |  |
| `data.object` | string |  |
| `data.timezone` | string |  |
| `data.updated_at` | string |  |

## Native endpoint

Through the native Monica CRM API, this operation is `GET /me` (base URL `https://app.monicahq.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-me.md) for the provider-specific parameters and requirements.

