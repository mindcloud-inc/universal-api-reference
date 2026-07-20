# OnePageCRM Universal API Examples

These examples use the MindCloud API key and OnePageCRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Users

Retrieves users from OnePageCRM.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-users?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/list-users?${params}`, {
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
      "accountRights": [
        "string"
      ],
      "accountRole": "string",
      "bccEmail": "ava@example.com",
      "companyName": "Ava Chen",
      "countryCode": "string",
      "email": "ava@example.com",
      "firstName": "Ava",
      "googleContactsEmail": {},
      "id": "string",
      "lastName": "Chen",
      "photoUrl": "https://example.com",
      "virtualGroupId": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Users action reference](actions/list-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onePageCRM/latest/actions/list-users).

## Change Contact Owner

Changes a contact's owner in OnePageCRM.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/change-contact-owner" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contactId": "Select a contact",
  "ownerId": "Select a user"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/onePageCRM/latest/actions/change-contact-owner', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contactId": "Select a contact",
    "ownerId": "Select a user"
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
      "address": {
        "address": {},
        "city": {},
        "countryCode": {},
        "state": {},
        "zipCode": {}
      },
      "contactsCount": 1,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "lastTimelineUpdate": "2026-05-07T12:00:00.000Z",
      "modifiedAt": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "phone": "string",
      "photoUrl": "https://example.com",
      "syncedStatusId": {},
      "syncedTags": {},
      "syncingStatus": true,
      "syncingTags": true,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Change Contact Owner action reference](actions/change-contact-owner.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/onePageCRM/latest/actions/change-contact-owner).
