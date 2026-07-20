# Satori Cyber Universal API Examples

These examples use the MindCloud API key and Satori Cyber connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Datastores

Retrieves datastore records from Satori Cyber.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/list-datastores?connectionId=$CONNECTION_ID&accountId=acc_123456" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "accountId": "acc_123456"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/satoriCyber/latest/actions/list-datastores?${params}`, {
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
      "records": [
        {}
      ]
    }
  ],
  "meta": {}
}
```

See the full [List Datastores action reference](actions/list-datastores.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/satoriCyber/latest/actions/list-datastores).
