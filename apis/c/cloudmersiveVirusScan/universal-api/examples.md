# Cloudmersive Virus Scan Universal API Examples

These examples use the MindCloud API key and Cloudmersive Virus Scan connection described in [authentication.md](authentication.md). Replace `$CONNECTION_ID` with the connection ID you copied from the Connections page.

## Scan Website for Threats

Scans a website for malicious content with Cloudmersive Virus Scan.

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-website-for-threats?connectionId=$CONNECTION_ID&url=https%3A%2F%2Fexample.com" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "url": "https://example.com"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/cloudmersiveVirusScan/latest/actions/scan-website-for-threats?${params}`, {
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
      "CleanResult": true,
      "FoundViruses": [
        {
          "FileName": "Ava Chen",
          "VirusName": "Ava Chen"
        }
      ],
      "WebsiteHttpResponseCode": 1,
      "WebsiteThreatType": "string"
    }
  ],
  "meta": {}
}
```

See the full [Scan Website for Threats action reference](actions/scan-website-for-threats.md), or [try it interactively](https://mindcloud.co/docs/universal/rest/cloudmersiveVirusScan/latest/actions/scan-website-for-threats).
