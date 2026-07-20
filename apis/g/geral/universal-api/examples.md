# Geral Universal API Examples

These examples use the MindCloud API key and Geral connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get User

Retrieves the current user from Geral.

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

Example response:

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

See the full [Get User action reference](actions/get-user.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/geral/latest/actions/get-user).
