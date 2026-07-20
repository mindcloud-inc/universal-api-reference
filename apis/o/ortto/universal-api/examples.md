# Ortto Universal API Examples

These examples use the MindCloud API key and Ortto connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Export Campaign Data



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/export-campaign-data?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ortto/latest/actions/export-campaign-data?${params}`, {
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
      "folderId": "string",
      "hasMore": true
    }
  ],
  "meta": {}
}
```

See the full [Export Campaign Data action reference](actions/export-campaign-data.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ortto/latest/actions/export-campaign-data).

## Archive Accounts



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/ortto/latest/actions/archive-accounts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "inclusion_ids[]": [
    "string"
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/ortto/latest/actions/archive-accounts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "inclusion_ids[]": ["string"]
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
      "archivedOrganizations": 1,
      "scheduledOrganizations": 1
    }
  ],
  "meta": {}
}
```

See the full [Archive Accounts action reference](actions/archive-accounts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/ortto/latest/actions/archive-accounts).
