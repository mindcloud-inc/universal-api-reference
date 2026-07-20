# FillFaster Universal API Examples

These examples use the MindCloud API key and FillFaster connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves a list of active forms from FillFaster.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/list-forms?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/list-forms?${params}`, {
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
      "created": "2026-05-07T12:00:00.000Z",
      "fid": "string",
      "name": "Ava Chen",
      "submissions": "string"
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fillFaster/latest/actions/list-forms).

## Create Bulk Submissions

Creates multiple submissions in FillFaster.

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/create-bulk-submissions" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "submissions[]": [
    {}
  ]
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/fillFaster/latest/actions/create-bulk-submissions', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "submissions[]": [{}]
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
      "error": "string",
      "status": 1,
      "submissionId": "string",
      "submissionLink": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Create Bulk Submissions action reference](actions/create-bulk-submissions.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/fillFaster/latest/actions/create-bulk-submissions).
