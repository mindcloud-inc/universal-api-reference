# Sendloop Universal API Examples

These examples use the MindCloud API key and Sendloop connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/list-lists?${params}`, {
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
      "activeSubscribers": 1,
      "createdOn": "2026-05-07T12:00:00.000Z",
      "listID": 1,
      "name": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendloop/latest/actions/list-lists).

## Create Campaign



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "fromName": "Ava Chen",
  "fromEmail": "ava@example.com",
  "replyToName": "Ava Chen",
  "replyToEmail": "ava@example.com",
  "recipients": "string",
  "subject": "string",
  "htmlContent": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendloop/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "fromName": "Ava Chen",
    "fromEmail": "ava@example.com",
    "replyToName": "Ava Chen",
    "replyToEmail": "ava@example.com",
    "recipients": "string",
    "subject": "string",
    "htmlContent": "string"
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
      "availableRecipients": 1,
      "campaignID": "string",
      "estimatedRecipients": 1,
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Create Campaign action reference](actions/create-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendloop/latest/actions/create-campaign).
