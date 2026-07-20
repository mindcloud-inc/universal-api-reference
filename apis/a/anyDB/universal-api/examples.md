# AnyDB Universal API Examples

These examples use the MindCloud API key and AnyDB connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Key And Email

Validates API key and email in AnyDB.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/validate-api-key-and-email?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/validate-api-key-and-email?${params}`, {
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
      "email": "ava@example.com",
      "reason": "string",
      "success": true
    }
  ],
  "meta": {}
}
```

See the full [Validate API Key And Email action reference](actions/validate-api-key-and-email.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anyDB/latest/actions/validate-api-key-and-email).

## Complete Upload

Completes an attachment upload in AnyDB.

```bash
curl -X PUT "https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/complete-upload" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "fileSize": 1,
  "teamId": "string",
  "databaseId": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/anyDB/latest/actions/complete-upload', {
  method: 'PUT',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "fileSize": 1,
    "teamId": "string",
    "databaseId": "string"
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

See the full [Complete Upload action reference](actions/complete-upload.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/anyDB/latest/actions/complete-upload).
