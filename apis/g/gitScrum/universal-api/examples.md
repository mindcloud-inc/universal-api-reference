# GitScrum Universal API Examples

These examples use the MindCloud API key and GitScrum connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Verify Authentication

Retrieves the authenticated GitScrum account details.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/verify-authentication?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/gitScrum/latest/actions/verify-authentication?${params}`, {
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
      "avatar": "string",
      "country_id": 1,
      "created_at": {},
      "email_offers": true,
      "email_product_updates": true,
      "email_weekly": true,
      "headline": "string",
      "id": 1,
      "language": "string",
      "location": "string",
      "name": "Ava Chen",
      "onboarding_completed": true,
      "onboarding_started": true,
      "presence_status": "string",
      "theme": "string",
      "timezone_id": 1,
      "timezone_name": "Ava Chen",
      "username": "Ava Chen",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Verify Authentication action reference](actions/verify-authentication.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/gitScrum/latest/actions/verify-authentication).
