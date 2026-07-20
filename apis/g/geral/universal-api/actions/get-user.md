# Geral: Get User

Retrieves the current user from Geral.

```
GET https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Geral `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-user?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/geral/latest/actions/get-user?${params}`, {
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
      "anti_phishing_code": true,
      "billing": {},
      "browser_language": "string",
      "browser_name": "Ava Chen",
      "city_name": "Ava Chen",
      "continent_code": "string",
      "country": "string",
      "datetime": "2026-05-07T12:00:00.000Z",
      "device_type": "string",
      "email": "ava@example.com",
      "id": 1,
      "ip": "string",
      "is_newsletter_subscribed": true,
      "language": "string",
      "last_activity": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "next_cleanup_datetime": "2026-05-07T12:00:00.000Z",
      "os_name": "Ava Chen",
      "payment_currency": "string",
      "payment_processor": "string",
      "payment_subscription_id": "string",
      "payment_total_amount": 1,
      "plan_expiration_date": "2026-05-07T12:00:00.000Z",
      "plan_id": "string",
      "plan_settings": {},
      "plan_trial_done": true,
      "referral_key": "string",
      "referred_by": "string",
      "source": "string",
      "status": true,
      "timezone": "string",
      "total_logins": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `anti_phishing_code` | boolean | Whether anti-phishing code is enabled. |
| `billing` | object | Billing profile details. |
| `browser_language` | string | Browser language. |
| `browser_name` | string | Browser name. |
| `city_name` | string | City name. |
| `continent_code` | string | Continent code. |
| `country` | string | Country code. |
| `datetime` | date | Account creation timestamp. |
| `device_type` | string | Device type. |
| `email` | string | User email address. |
| `id` | number | Geral user ID. |
| `ip` | string | Last known IP address. |
| `is_newsletter_subscribed` | boolean | Whether newsletter subscription is enabled. |
| `language` | string | Account language. |
| `last_activity` | date | Last activity timestamp. |
| `name` | string | User display name. |
| `next_cleanup_datetime` | date | Next cleanup timestamp. |
| `os_name` | string | Operating system name. |
| `payment_currency` | string | Payment currency. |
| `payment_processor` | string | Payment processor name. |
| `payment_subscription_id` | string | Payment subscription identifier. |
| `payment_total_amount` | number | Total payment amount. |
| `plan_expiration_date` | date | Plan expiration date. |
| `plan_id` | string | Plan identifier. |
| `plan_settings` | object | Plan feature settings. |
| `plan_trial_done` | boolean | Whether the plan trial is completed. |
| `referral_key` | string | Referral key. |
| `referred_by` | string | Referring user, when present. |
| `source` | string | Signup source. |
| `status` | boolean | Whether the account is active. |
| `timezone` | string | Account timezone. |
| `total_logins` | number | Total login count. |

## Native endpoint

Through the native Geral API, this operation is `GET /user` (base URL `https://ger.al/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-user.md) for the provider-specific parameters and requirements.

