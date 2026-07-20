# Jitbit Helpdesk Universal API Examples

These examples use the MindCloud API key and Jitbit Helpdesk connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Get Attachment



```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-attachment?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/jitbitHelpdesk/latest/actions/get-attachment?${params}`, {
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
      "fileId": 1,
      "fileName": "Ava Chen",
      "fileSize": 1,
      "issueId": 1,
      "url": "https://example.com"
    }
  ],
  "meta": {}
}
```

See the full [Get Attachment action reference](actions/get-attachment.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/jitbitHelpdesk/latest/actions/get-attachment).
