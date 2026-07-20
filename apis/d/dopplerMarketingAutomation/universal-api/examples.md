# Doppler Marketing Automation Universal API Examples

These examples use the MindCloud API key and Doppler Marketing Automation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Lists

Retrieves lists from Doppler Marketing Automation.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/list-lists?${params}`, {
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
      "_links": [
        {}
      ],
      "currentPage": 1,
      "items": [
        {}
      ],
      "itemsCount": 1,
      "pagesCount": 1,
      "pageSize": 1
    }
  ],
  "meta": {}
}
```

See the full [List Lists action reference](actions/list-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dopplerMarketingAutomation/latest/actions/list-lists).

## Associate Subscriber

Creates a subscriber association in Doppler Marketing Automation.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/associate-subscriber" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listId": "509702",
  "email": "subscriber@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/dopplerMarketingAutomation/latest/actions/associate-subscriber', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listId": "509702",
    "email": "subscriber@example.com"
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
      "_links": [
        {}
      ],
      "message": "string"
    }
  ],
  "meta": {}
}
```

See the full [Associate Subscriber action reference](actions/associate-subscriber.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/dopplerMarketingAutomation/latest/actions/associate-subscriber).
