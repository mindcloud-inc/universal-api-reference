# Paperform Universal API Examples

These examples use the MindCloud API key and Paperform connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## List Forms

Retrieves forms from Paperform.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-forms?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/paperform/latest/actions/list-forms?${params}`, {
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
      "accountTimezone": "string",
      "additionalUrls": {
        "duplicateUrl": "https://example.com",
        "editUrl": "https://example.com",
        "submissionsUrl": "https://example.com"
      },
      "coverImageUrl": "https://example.com",
      "createdAt": "string",
      "createdAtUtc": "2026-05-07T12:00:00.000Z",
      "description": "string",
      "id": "string",
      "live": true,
      "slug": "string",
      "spaceId": 1,
      "submissionCount": 1,
      "title": "string",
      "updatedAt": "string",
      "updatedAtUtc": "2026-05-07T12:00:00.000Z",
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [List Forms action reference](actions/list-forms.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/paperform/latest/actions/list-forms).
