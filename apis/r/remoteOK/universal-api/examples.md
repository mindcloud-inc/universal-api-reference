# Remote OK Universal API Examples

These examples use the MindCloud API key and Remote OK connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Remote Jobs

Retrieves remote job postings from Remote OK.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/remoteOK/latest/actions/list-remote-jobs?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/remoteOK/latest/actions/list-remote-jobs?${params}`, {
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
      "apply_url": "https://example.com",
      "company": "Ava Chen",
      "company_logo": "https://example.com",
      "date": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "epoch": 1,
      "id": "string",
      "location": "string",
      "logo": "https://example.com",
      "original": true,
      "position": "string",
      "salary_max": 1,
      "salary_min": 1,
      "slug": "string",
      "tags": [
        "string"
      ],
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Remote Jobs action reference](actions/list-remote-jobs.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/remoteOK/latest/actions/list-remote-jobs).
