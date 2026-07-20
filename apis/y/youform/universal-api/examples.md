# Youform Universal API Examples

These examples use the MindCloud API key and Youform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get My Profile

Retrieves your profile from Youform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/youform/latest/actions/get-my-profile?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/youform/latest/actions/get-my-profile?${params}`, {
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
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": 1,
      "lastName": "Chen"
    }
  ],
  "meta": {}
}
```

See the full [Get My Profile action reference](actions/get-my-profile.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youform/latest/actions/get-my-profile).

## Create Webhook

Creates a webhook in Youform.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/youform/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "formSlug": "string",
  "webhookUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/youform/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "formSlug": "string",
    "webhookUrl": "https://example.com"
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
      "id": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/youform/latest/actions/create-webhook).
