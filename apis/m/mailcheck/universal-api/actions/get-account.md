# Mailcheck: Get Account



```
GET https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/get-account
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Mailcheck `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/get-account?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailcheck/latest/actions/get-account?${params}`, {
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
      "api_key": {
        "created_at": "string",
        "last_used_at": "string",
        "prefix": "string"
      },
      "email": "ava@example.com",
      "monthly_limit": 1,
      "plan": "string",
      "usage": {
        "current_month": 1,
        "remaining": 1
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `api_key` | object | Metadata about the active API key. |
| `api_key.created_at` | string | When the API key was created. |
| `api_key.last_used_at` | string | When the API key was last used. |
| `api_key.prefix` | string | Visible prefix of the current API key. |
| `email` | string | Account email address. |
| `monthly_limit` | number | Monthly verification quota for the account. |
| `plan` | string | Current MailCheck billing plan. |
| `usage` | object | Current usage summary. |
| `usage.current_month` | number | Verifications used this month. |
| `usage.remaining` | number | Verifications remaining this month. |

## Native endpoint

Through the native Mailcheck API, this operation is `GET /v1/account` (base URL `https://api.mailcheck.dev`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-account.md) for the provider-specific parameters and requirements.

