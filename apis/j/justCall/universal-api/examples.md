# JustCall Universal API Examples

These examples use the MindCloud API key and JustCall connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List All Users

Retrieves users from JustCall.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-users?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/justCall/latest/actions/list-all-users?${params}`, {
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
      "count": 1,
      "currentPage": 1,
      "data": [
        {}
      ],
      "nextPageLink": "https://example.com",
      "perPage": 1,
      "prevPageLink": "https://example.com",
      "status": "string",
      "totalCount": 1
    }
  ],
  "meta": {}
}
```

See the full [List All Users action reference](actions/list-all-users.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/justCall/latest/actions/list-all-users).

## Bulk Add Contacts to Blacklist

Adds contacts to the JustCall blacklist.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/justCall/latest/actions/bulk-add-contacts-to-blacklist" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "addTo[]": [
    "string"
  ],
  "contactNumbers[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/justCall/latest/actions/bulk-add-contacts-to-blacklist', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "addTo[]": ["string"],
    "contactNumbers[]": ["string"]
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
      "data": {},
      "status": "string"
    }
  ],
  "meta": {}
}
```

See the full [Bulk Add Contacts to Blacklist action reference](actions/bulk-add-contacts-to-blacklist.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/justCall/latest/actions/bulk-add-contacts-to-blacklist).
