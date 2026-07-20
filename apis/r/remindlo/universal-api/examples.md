# Remindlo Universal API Examples

These examples use the MindCloud API key and Remindlo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Campaigns



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/list-campaigns?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/list-campaigns?${params}`, {
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
      "campaigns": [
        {}
      ],
      "pagination": {},
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [List Campaigns action reference](actions/list-campaigns.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remindlo/latest/actions/list-campaigns).

## Create Webhook



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/create-webhook" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "eventTypes[]": [
    "string"
  ],
  "name": "Ava Chen",
  "targetUrl": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remindlo/latest/actions/create-webhook', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "eventTypes[]": ["string"],
    "name": "Ava Chen",
    "targetUrl": "https://example.com"
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
      "endpoint": {},
      "signing_secret": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Webhook action reference](actions/create-webhook.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remindlo/latest/actions/create-webhook).
