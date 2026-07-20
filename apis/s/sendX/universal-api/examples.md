# SendX Universal API Examples

These examples use the MindCloud API key and SendX connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-contacts?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/sendX/latest/actions/list-contacts?${params}`, {
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
      "blocked": true,
      "bounced": true,
      "company": "string",
      "contactSource": 1,
      "created": "2026-05-07T12:00:00.000Z",
      "customFields": {},
      "dropped": true,
      "email": "ava@example.com",
      "firstName": "Ava",
      "id": "string",
      "lastName": "Chen",
      "lastTrackedIp": "string",
      "lists": [
        "string"
      ],
      "LTV": 1,
      "pageSource": "string",
      "spam": true,
      "tags": [
        "string"
      ],
      "trackData": "string",
      "unsubscribed": true,
      "updated": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendX/latest/actions/list-contacts).

## Create Campaign



```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/sendX/latest/actions/create-campaign" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "name": "Ava Chen",
  "subject": "string",
  "sender": "string",
  "htmlCode": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/sendX/latest/actions/create-campaign', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "name": "Ava Chen",
    "subject": "string",
    "sender": "string",
    "htmlCode": "string"
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
      "campaignScreenshotUrl": "https://example.com",
      "excludedLists": [
        "string"
      ],
      "excludedSegments": [
        "string"
      ],
      "excludedTags": [
        "string"
      ],
      "id": "string",
      "includedLists": [
        "string"
      ],
      "includedSegments": [
        "string"
      ],
      "includedTags": [
        "string"
      ],
      "isArchived": true,
      "name": "Ava Chen",
      "preferredTimeCondition": "string",
      "preferredTimezone": "string",
      "scheduleCondition": "string",
      "scheduleType": 1,
      "sender": "string",
      "sendInContactsTimezone": true,
      "smartSend": true,
      "status": 1,
      "strategy": "string",
      "subject": "string",
      "timeCondition": "string",
      "timezone": "string"
    }
  ],
  "meta": {}
}
```

See the full [Create Campaign action reference](actions/create-campaign.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/sendX/latest/actions/create-campaign).
