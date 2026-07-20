# CaptureIQ Universal API Examples

These examples use the MindCloud API key and CaptureIQ connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Validate API Key

Retrieves API key validation status from CaptureIQ.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/captureIQ/latest/actions/validate-api-key?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/captureIQ/latest/actions/validate-api-key?${params}`, {
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
      "status": true
    }
  ],
  "meta": {}
}
```

See the full [Validate API Key action reference](actions/validate-api-key.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/captureIQ/latest/actions/validate-api-key).
