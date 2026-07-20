# Bigin by Zoho CRM Universal API Examples

These examples use the MindCloud API key and Bigin by Zoho CRM connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Count Records

Counts records in a Bigin by Zoho CRM module.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/count-records?connectionId=$CONNECTION_ID&moduleApiName=Ava%20Chen" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "moduleApiName": "Ava Chen"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/count-records?${params}`, {
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
  "data": [],
  "meta": {}
}
```

See the full [Count Records action reference](actions/count-records.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/biginByZohoCRM/latest/actions/count-records).

## Add Notes

Creates standalone notes in Bigin by Zoho CRM.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/add-notes" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "data[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/biginByZohoCRM/latest/actions/add-notes', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "data[]": [{}]
  })
});

const { success, data } = await response.json();
```

Example response:

```json
{
  "success": true,
  "data": [],
  "meta": {}
}
```

See the full [Add Notes action reference](actions/add-notes.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/biginByZohoCRM/latest/actions/add-notes).
