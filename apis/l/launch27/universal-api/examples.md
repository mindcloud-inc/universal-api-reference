# Launch27 Universal API Examples

These examples use the MindCloud API key and Launch27 connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get General Settings

Retrieves general settings from Launch27.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-general-settings?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/launch27/latest/actions/get-general-settings?${params}`, {
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
      "addons": [
        {}
      ],
      "google_analytics_id": "string",
      "google_analytics_marketing_id": "string",
      "google_api_key": "string",
      "google_tag_manager_id": "string",
      "intercom_app_id": "string",
      "leads": [
        {}
      ],
      "locales": [
        {}
      ],
      "plans": [
        {}
      ],
      "stripe_public_key": "string",
      "trial_days": 1
    }
  ],
  "meta": {}
}
```

See the full [Get General Settings action reference](actions/get-general-settings.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/launch27/latest/actions/get-general-settings).

## Authorize Billing Charge

Authorizes a billing charge in Launch27.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/launch27/latest/actions/authorize-billing-charge" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "token": "string",
  "stripe_setup_intent_id": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/launch27/latest/actions/authorize-billing-charge', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "token": "string",
    "stripe_setup_intent_id": "string"
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [
    {
      "stripe_payment_intent_secret": "string",
      "stripe_requires_action": true,
      "stripe_setup_intent_secret": "string"
    }
  ],
  "meta": {}
}
```

See the full [Authorize Billing Charge action reference](actions/authorize-billing-charge.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/launch27/latest/actions/authorize-billing-charge).
