# Referral Rock Universal API Examples

These examples use the MindCloud API key and Referral Rock connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Programs

Retrieves referral programs from Referral Rock.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-programs?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/list-programs?${params}`, {
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
      "directUrl": "https://example.com",
      "id": "string",
      "isActive": true,
      "memberOffer": "string",
      "name": "Ava Chen",
      "referralOffer": "string",
      "title": "string",
      "type": "string",
      "widgetUrl": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Programs action reference](actions/list-programs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/referralRock/latest/actions/list-programs).

## Create Hook

Creates a webhook subscription in Referral Rock.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-hook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "targetUrl": "https://example.com",
  "event": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/referralRock/latest/actions/create-hook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "targetUrl": "https://example.com",
    "event": "string"
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
      "web_hook_id": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Hook action reference](actions/create-hook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/referralRock/latest/actions/create-hook).
