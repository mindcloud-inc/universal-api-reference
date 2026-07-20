# Easy Email Verification Universal API Examples

These examples use the MindCloud API key and Easy Email Verification connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Bulk Jobs

Retrieves all bulk job statuses from Easy Email Verification.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/list-bulk-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/list-bulk-jobs?${params}`, {
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

See the full [List Bulk Jobs action reference](actions/list-bulk-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyEmailVerification/latest/actions/list-bulk-jobs).

## Upload Bulk Email File

Creates a bulk verification job in Easy Email Verification.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/upload-bulk-email-file" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "file": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/easyEmailVerification/latest/actions/upload-bulk-email-file', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "file": "string"
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

See the full [Upload Bulk Email File action reference](actions/upload-bulk-email-file.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/easyEmailVerification/latest/actions/upload-bulk-email-file).
