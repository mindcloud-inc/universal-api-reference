# MailoPost Universal API Examples

These examples use the MindCloud API key and MailoPost connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Balance

Retrieves account balance details from MailoPost.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-balance?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/get-balance?${params}`, {
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
      "balance": 1,
      "tariff": {
        "credits": 1,
        "expires_at": 1,
        "subscribers": {
          "available": 1,
          "total": 1
        }
      }
    }
  ],
  "meta": {}
}
```

See the full [Get Balance action reference](actions/get-balance.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailoPost/latest/actions/get-balance).

## Create Campaign

Creates a new campaign in MailoPost.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fromEmail": "ava@example.com",
  "subject": "string",
  "html": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/mailoPost/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fromEmail": "ava@example.com",
    "subject": "string",
    "html": "string"
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
      "from_email": "ava@example.com",
      "from_name": "Ava Chen",
      "html": "string",
      "id": 1,
      "purchase": {
        "credits": 1,
        "deficit": 1,
        "enable": true,
        "subscribers": 1
      },
      "recipients_count": 1,
      "state": "string",
      "statistics": {
        "bounced": 1,
        "delivered": 1
      },
      "text": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Campaign action reference](actions/create-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mailoPost/latest/actions/create-campaign).
