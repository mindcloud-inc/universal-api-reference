# HelpDesk Universal API Examples

These examples use the MindCloud API key and HelpDesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Tickets

Retrieves tickets from HelpDesk.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-tickets?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/helpDesk/latest/actions/list-tickets?${params}`, {
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
      "assignment": {
        "team": {
          "ID": "string",
          "name": "Ava Chen"
        }
      },
      "cc": [
        {}
      ],
      "childTickets": [
        {}
      ],
      "createdAt": "2026-05-07T12:00:00.000Z",
      "createdBy": "string",
      "createdByType": "string",
      "detectedLanguage": "string",
      "events": [
        {}
      ],
      "followers": [
        "string"
      ],
      "ID": "string",
      "integrations": {},
      "lastMessageAt": "2026-05-07T12:00:00.000Z",
      "licenseID": 1,
      "priority": 1,
      "ratingRequestSent": true,
      "requester": {
        "email": "ava@example.com",
        "name": "Ava Chen"
      },
      "shortID": "string",
      "source": {
        "detailedSource": "string",
        "type": "string"
      },
      "spam": {
        "status": true
      },
      "status": "string",
      "subject": "string",
      "tagIDs": [
        "string"
      ],
      "teamIDs": [
        "string"
      ],
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "updatedBy": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Tickets action reference](actions/list-tickets.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/helpDesk/latest/actions/list-tickets).
