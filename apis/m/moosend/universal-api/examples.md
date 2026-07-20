# Moosend Universal API Examples

These examples use the MindCloud API key and Moosend connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Active Mailing Lists

Retrieves active mailing lists from Moosend.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-active-mailing-lists?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/moosend/latest/actions/list-active-mailing-lists?${params}`, {
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
      "activeMemberCount": 1,
      "bouncedMemberCount": 1,
      "createdBy": "string",
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customFieldsDefinition": [
        {}
      ],
      "id": "string",
      "importOperation": {},
      "name": "Ava Chen",
      "preferences": {},
      "removedMemberCount": 1,
      "status": 1,
      "unsubscribedMemberCount": 1,
      "updatedBy": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [List Active Mailing Lists action reference](actions/list-active-mailing-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moosend/latest/actions/list-active-mailing-lists).

## Add Multiple Subscribers

Creates multiple subscribers in Moosend.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/moosend/latest/actions/add-multiple-subscribers" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "mailingListId": "string",
  "subscribers": {}
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/moosend/latest/actions/add-multiple-subscribers', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "mailingListId": "string",
    "subscribers": {}
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
      "createdOn": "2026-05-07T12:00:00.000Z",
      "customFields": [
        {}
      ],
      "email": "ava@example.com",
      "id": "string",
      "name": "Ava Chen",
      "removedOn": "string",
      "subscribeMethod": 1,
      "subscribeType": 1,
      "tags": [
        "string"
      ],
      "unsubscribedFromID": "string",
      "unsubscribedOn": "string",
      "updatedOn": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

See the full [Add Multiple Subscribers action reference](actions/add-multiple-subscribers.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/moosend/latest/actions/add-multiple-subscribers).
