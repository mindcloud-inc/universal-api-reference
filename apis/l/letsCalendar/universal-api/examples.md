# Let's Calendar Universal API Examples

These examples use the MindCloud API key and Let's Calendar connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Senders

Retrieves sender emails from Let's Calendar.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-senders?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/list-senders?${params}`, {
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
      "senderEmails": [
        {
          "email": "ava@example.com",
          "id": 1,
          "name": "ava@example.com",
          "providerName": "ava@example.com",
          "replyTo": "ava@example.com"
        }
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Senders action reference](actions/list-senders.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/letsCalendar/latest/actions/list-senders).

## Add Multiple Contacts to Campaign

Adds multiple contacts to a campaign in Let's Calendar.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/add-multiple-contacts-to-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "campaignId": "string",
  "contacts[].firstname": "Ava",
  "contacts[].email": "ava@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/letsCalendar/latest/actions/add-multiple-contacts-to-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "campaignId": "string",
    "contacts[].firstname": "Ava",
    "contacts[].email": "ava@example.com"
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
      "duplicateCount": 1,
      "duplicateEmails": [
        [
          "ava@example.com"
        ]
      ],
      "invalidCount": 1,
      "message": "string",
      "validCount": 1
    }
  ],
  "meta": {}
}
```

See the full [Add Multiple Contacts to Campaign action reference](actions/add-multiple-contacts-to-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/letsCalendar/latest/actions/add-multiple-contacts-to-campaign).
