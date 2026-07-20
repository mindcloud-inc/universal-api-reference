# Zoho Campaigns Universal API Examples

These examples use the MindCloud API key and Zoho Campaigns connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Mailing Lists

Retrieves mailing lists from Zoho Campaigns.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-mailing-lists?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/list-mailing-lists?${params}`, {
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
      "createdTime": "string",
      "createdTimeGmt": "string",
      "date": "string",
      "deletable": "string",
      "editable": "string",
      "isPublic": "string",
      "issmart": "string",
      "listCampaignsCount": "string",
      "listCreatedDate": "string",
      "listCreatedTime": "string",
      "listdesc": "string",
      "listdgs": "string",
      "listkey": "string",
      "listname": "Ava Chen",
      "listnotifications": "string",
      "listtype": "string",
      "listunino": "string",
      "lockstatus": "string",
      "noofbouncecnt": "string",
      "noofcontacts": "string",
      "noofunsubcnt": "string",
      "otherslist": "string",
      "owner": "string",
      "segments": {},
      "sentcnt": "string",
      "servicetype": "string",
      "sno": "string",
      "updatedTimeGmt": "string",
      "zuid": "string",
      "zx": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Mailing Lists action reference](actions/list-mailing-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCampaigns/latest/actions/list-mailing-lists).

## Add List Contacts in Bulk

Adds contacts to a Zoho Campaigns list in bulk.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/add-list-contacts-in-bulk" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "listKey": "string",
  "emailIds": "alice@example.com,bob@example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/zohoCampaigns/latest/actions/add-list-contacts-in-bulk', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "listKey": "string",
    "emailIds": "alice@example.com,bob@example.com"
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
      "code": "string",
      "existingContacts": [
        "string"
      ],
      "ignoredContacts": [
        "string"
      ],
      "listkey": "string",
      "listname": "Ava Chen",
      "readdContacts": [
        "string"
      ],
      "status": "string",
      "url": "https://example.com",
      "version": "string"
    }
  ],
  "meta": {}
}
```

See the full [Add List Contacts in Bulk action reference](actions/add-list-contacts-in-bulk.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/zohoCampaigns/latest/actions/add-list-contacts-in-bulk).
