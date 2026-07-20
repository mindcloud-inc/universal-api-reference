# EmailVerify.io: Check Account Balance

Retrieves account balance details from EmailVerify.io.

```
GET https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/check-account-balance
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a EmailVerify.io `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/check-account-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/emailVerifyio/latest/actions/check-account-balance?${params}`, {
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
      "apiStatus": "string",
      "bonusCredits": 1,
      "dailyCreditsLimit": 1,
      "remainingCredits": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `apiStatus` | string | Whether the EmailVerify.io API is enabled. |
| `bonusCredits` | number | Bonus credits currently available. |
| `dailyCreditsLimit` | number | Daily credit cap for the account. |
| `remainingCredits` | number | Remaining verification credits. |

## Native endpoint

Through the native EmailVerify.io API, this operation is `GET /check-account-balance/` (base URL `https://app.emailverify.io/api/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/check-account-balance.md) for the provider-specific parameters and requirements.

