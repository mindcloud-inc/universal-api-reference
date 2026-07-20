# Remarkety Universal API Examples

These examples use the MindCloud API key and Remarkety connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Batch Upsert Contacts



```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/batch-upsert-contacts" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "contacts[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/remarkety/latest/actions/batch-upsert-contacts', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "contacts[]": [{}]
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
      "failed": 1,
      "failedReason": [
        {}
      ],
      "success": 1
    }
  ],
  "meta": {}
}
```

See the full [Batch Upsert Contacts action reference](actions/batch-upsert-contacts.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remarkety/latest/actions/batch-upsert-contacts).
