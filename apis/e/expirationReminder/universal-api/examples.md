# Expiration Reminder Universal API Examples

These examples use the MindCloud API key and Expiration Reminder connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Contacts

Retrieves contacts from Expiration Reminder.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-contacts?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/list-contacts?${params}`, {
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
      "assignedTo": {},
      "contactId": "string",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "id": "string",
      "isActive": true,
      "locationId": "string",
      "mobile": "string",
      "modified": "string",
      "name": "Ava Chen",
      "phone": "string",
      "teamId": "string",
      "timezone": "string",
      "typeId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Contacts action reference](actions/list-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/expirationReminder/latest/actions/list-contacts).

## Add File to Expiration Item

Adds a file to an expiration item in Expiration Reminder.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/add-file-to-expiration-item" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/expirationReminder/latest/actions/add-file-to-expiration-item', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId
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
      "assignedTo": {},
      "attachments": [
        {}
      ],
      "category": {},
      "categoryName": "Ava Chen",
      "contactId": "string",
      "contacts": [
        {}
      ],
      "customFields": [
        {}
      ],
      "details": "string",
      "expirationDate": "string",
      "id": "string",
      "isActive": true,
      "locations": [
        {}
      ],
      "modified": "string",
      "name": "Ava Chen",
      "status": "string",
      "statusId": 1,
      "tags": [
        {}
      ],
      "teamId": "string",
      "timeOfDay": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add File to Expiration Item action reference](actions/add-file-to-expiration-item.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/expirationReminder/latest/actions/add-file-to-expiration-item).
