# Mime Automation Universal API Examples

These examples use the MindCloud API key and Mime Automation connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Extract Files From TNEF

Retrieves attachments from a TNEF-encoded file in Mime Automation.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-tnef?connectionId=$CONNECTION_ID&content=Paste%20base64-encoded%20TNEF%20content" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "content": "Paste base64-encoded TNEF content"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/mimeAutomation/latest/actions/extract-files-from-tnef?${params}`, {
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
      "content": "string",
      "fileName": "Ava Chen"
    }
  ],
  "meta": {}
}
```

See the full [Extract Files From TNEF action reference](actions/extract-files-from-tnef.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/mimeAutomation/latest/actions/extract-files-from-tnef).
