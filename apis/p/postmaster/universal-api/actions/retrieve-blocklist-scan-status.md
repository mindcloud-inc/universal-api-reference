# Postmaster+: Retrieve Blocklist Scan Status

Retrieves blocklist scan status from Postmaster+.

```
GET https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-blocklist-scan-status
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Postmaster+ `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-blocklist-scan-status?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/postmaster/latest/actions/retrieve-blocklist-scan-status?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as query string parameters ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `id` | string | yes | The ULID of the blocklist check. |

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

Through the native Postmaster+ API, this operation is `GET /api/v1/blocklist/scan/status/:id` (base URL `https://postmasterplus.app`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/retrieve-blocklist-scan-status.md) for the provider-specific parameters and requirements.

