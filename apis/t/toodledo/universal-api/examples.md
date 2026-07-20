# Toodledo Universal API Examples

These examples use the MindCloud API key and Toodledo connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Account Info

Retrieves account details from Toodledo.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/get-account-info?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/get-account-info?${params}`, {
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
      "alias": "string",
      "dateformat": 1,
      "email": "ava@example.com",
      "hidemonths": 1,
      "hotlistduedate": 1,
      "hotlistpriority": 1,
      "lastdelete_note": 1,
      "lastdelete_task": 1,
      "lastedit_context": 1,
      "lastedit_folder": 1,
      "lastedit_goal": 1,
      "lastedit_list": 1,
      "lastedit_location": 1,
      "lastedit_note": 1,
      "lastedit_outline": 1,
      "lastedit_task": 1,
      "pro": 1,
      "showtabnums": 1,
      "timezone": 1,
      "userid": "string"
    }
  ],
  "meta": {}
}
```

See the full [Get Account Info action reference](actions/get-account-info.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/toodledo/latest/actions/get-account-info).

## Create Lists

Creates lists in Toodledo.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-lists" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "lists": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/toodledo/latest/actions/create-lists', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "lists": "string"
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
      "added": 1,
      "cols": [
        {}
      ],
      "id": "string",
      "keywords": "string",
      "modified": 1,
      "note": "string",
      "ref": "string",
      "rows": 1,
      "title": "string",
      "version": 1
    }
  ],
  "meta": {}
}
```

See the full [Create Lists action reference](actions/create-lists.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/toodledo/latest/actions/create-lists).
