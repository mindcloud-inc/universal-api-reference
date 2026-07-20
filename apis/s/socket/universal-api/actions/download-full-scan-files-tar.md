# Socket: Download Full Scan Files Tar

Downloads a full scan tarball from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/download-full-scan-files-tar
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/download-full-scan-files-tar?connectionId=$CONNECTION_ID&fullScanId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "fullScanId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/download-full-scan-files-tar?${params}`, {
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
| `fullScanId` | string | yes |  |

## Response

The response envelope is `{ "success": true, "data": [...], "meta": {} }`. The `data` schema for this action is dynamic; it mirrors what the native Socket API returns.

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/full-scans/:full_scan_id/files/tar` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/download-full-scan-files-tar.md) for the provider-specific parameters and requirements.

