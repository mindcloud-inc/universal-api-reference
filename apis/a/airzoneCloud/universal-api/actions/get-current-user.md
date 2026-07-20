# Airzone Cloud: Get Current User

Retrieves the current user profile from Airzone Cloud.

```
GET https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-current-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Airzone Cloud `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-current-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/airzoneCloud/latest/actions/get-current-user?${params}`, {
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
      "_id": "string",
      "config": {},
      "confirmation_date": "string",
      "created_at": "string",
      "data": {},
      "email": "ava@example.com"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `_id` | string | User unique ID. |
| `config` | object | User configuration object. |
| `confirmation_date` | string | Account confirmation timestamp. |
| `created_at` | string | Account creation timestamp. |
| `data` | object | User personal data object. |
| `email` | string | User email. |

## Native endpoint

Through the native Airzone Cloud API, this operation is `GET /user/` (base URL `https://m.airzonecloud.com/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-current-user.md) for the provider-specific parameters and requirements.

