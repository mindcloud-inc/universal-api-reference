# CallerAPI: Get Balance and Email

Retrieves account balance and email from CallerAPI.

```
GET https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/get-balance-and-email
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CallerAPI `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/get-balance-and-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/callerAPI/latest/actions/get-balance-and-email?${params}`, {
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
      "credits_left": 1,
      "credits_monthly": 1,
      "credits_spent": 1,
      "email": "ava@example.com",
      "status": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits_left` | number | Amount of credits left in the account. |
| `credits_monthly` | number | Total monthly credits available on the account. |
| `credits_spent` | number | Amount of credits already spent. |
| `email` | string | Account email address. |
| `status` | string | CallerAPI response status. |

## Native endpoint

Through the native CallerAPI API, this operation is `GET /api/me` (base URL `https://api.callerapi.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-balance-and-email.md) for the provider-specific parameters and requirements.

