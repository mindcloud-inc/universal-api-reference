# Postmaster+: Start Blocklist Scan

Starts a blocklist scan in Postmaster+.

```
POST https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/start-blocklist-scan
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/start-blocklist-scan" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "urls": "https://example.com"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/start-blocklist-scan', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "urls": "https://example.com"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `followRedirects` | boolean | no | Whether to follow redirects and scan all hosts in the redirect chain. |
| `urls` | list<string> | yes | Array of URLs to scan, between 1 and 100 URLs. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "blocklisted": true,
      "completedAt": "string",
      "creditsUsed": 1,
      "errorMessage": "string",
      "id": "string",
      "message": "string",
      "startedAt": "string",
      "status": "string",
      "totalHostsDetected": "string",
      "uniqueHostsChecked": 1,
      "urlsScanned": 1,
      "urlsSkipped": 1
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `blocklisted` | boolean | Whether any host is blocklisted. |
| `completedAt` | string | Completion timestamp. |
| `creditsUsed` | number | Credits consumed. |
| `errorMessage` | string | Provider error message. |
| `id` | string | Blocklist check ULID. |
| `message` | string | Provider message. |
| `startedAt` | string | Start timestamp. |
| `status` | string | Check status. |
| `totalHostsDetected` | string | Number of detected hosts when available. |
| `uniqueHostsChecked` | number | Number of unique hosts checked. |
| `urlsScanned` | number | Number of scanned URLs. |
| `urlsSkipped` | number | Number of skipped URLs. |

## Native endpoint

Through the native Postmaster+ API, this operation is `POST /api/v1/blocklist/scan/start` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/start-blocklist-scan.md) for the provider-specific parameters and requirements.

