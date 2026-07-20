# Dreamstudio: Get Account Details

Retrieves authenticated account details from Dreamstudio.

```
GET https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-account-details
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Dreamstudio `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-account-details?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dreamstudio/latest/actions/get-account-details?${params}`, {
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
      "email": "ava@example.com",
      "id": "string",
      "organizations": [
        {}
      ],
      "profile_picture": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `email` | string | Email address on the Stability account. |
| `id` | string | Stability account user id. |
| `organizations` | array<object> | Organizations available to the authenticated user. |
| `profile_picture` | string | Profile image URL when available. |

## Native endpoint

Through the native Dreamstudio API, this operation is `GET /v1/user/account` (base URL `https://api.stability.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account-details.md) for the provider-specific parameters and requirements.

