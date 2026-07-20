# Extruct AI: Get User

Retrieves the authenticated user from Extruct AI.

```
GET https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Extruct AI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/extructAI/latest/actions/get-user?${params}`, {
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
      "availableCredits": 1,
      "email": "ava@example.com",
      "organizationId": {},
      "organizationIsActive": {},
      "organizationName": {},
      "organizationSlug": {},
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `availableCredits` | number |  |
| `email` | string |  |
| `organizationId` | object |  |
| `organizationIsActive` | object |  |
| `organizationName` | object |  |
| `organizationSlug` | object |  |
| `userId` | string |  |

## Native endpoint

Through the native Extruct AI API, this operation is `GET /v1/user` (base URL `https://api.extruct.ai`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

