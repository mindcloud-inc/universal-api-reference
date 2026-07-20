# Scrapeless: Get User Info

Retrieves user information from Scrapeless.

```
GET https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-user-info
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Scrapeless `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-user-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/scrapeless/latest/actions/get-user-info?${params}`, {
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
      "credits": "string",
      "excessCredits": "string",
      "plan": {
        "credits": "string",
        "endAt": "string",
        "price": 1,
        "status": 1,
        "usage": 1
      },
      "status": 1,
      "userId": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `credits` | string | The user's account balance as a string. |
| `excessCredits` | string | The user's remaining credits (if applicable), as a string. |
| `plan` | object | Details about the user's subscription plan. |
| `plan.credits` | string | Remaining balance within the subscription plan, as a string. |
| `plan.endAt` | string | Subscription plan expiry date in ISO 8601 format. |
| `plan.price` | number | The price of the subscription plan, as a number. |
| `plan.status` | number | The status of the subscription plan (0 for inactive). |
| `plan.usage` | number | The current usage of the subscription plan, as a number. |
| `status` | number | General user status (1 for active users). |
| `userId` | string | The unique identifier of the user. |

## Native endpoint

Through the native Scrapeless API, this operation is `GET /api/v1/me` (base URL `https://api.scrapeless.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user-info.md) for the provider-specific parameters and requirements.

