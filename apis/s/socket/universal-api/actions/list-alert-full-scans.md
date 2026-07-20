# Socket: List Alert Full Scans

Retrieves full scans associated with alerts from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alert-full-scans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alert-full-scans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alert-full-scans?${params}`, {
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
| `alertKey` | string | no |  |
| `perPage` | string | no |  |
| `range` | string | no |  |
| `startAfterCursor` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "endCursor": "string",
      "items": [
        {
          "alertKeys": [
            "string"
          ],
          "branchName": "Ava Chen",
          "branchType": "string",
          "fullScanId": "string",
          "repoFullName": "Ava Chen",
          "sbomCreatedAt": "string",
          "scannedAt": "string"
        }
      ],
      "meta": {
        "alertKeys": [
          "string"
        ],
        "endDateInclusive": "string",
        "organizationId": "string",
        "queryStartTimestamp": 1,
        "startDateInclusive": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `endCursor` | string |  |
| `items` | array<object> |  |
| `items[]` | object |  |
| `items[].alertKeys` | array<string> |  |
| `items[].branchName` | string |  |
| `items[].branchType` | string | Type of branch that was scanned |
| `items[].fullScanId` | string | ID of full scan |
| `items[].repoFullName` | string | Full name of repo which contains repo workspace and repo slug |
| `items[].sbomCreatedAt` | string | ISO date when SBOM was created |
| `items[].scannedAt` | string | ISO date when SBOM was scanned |
| `meta` | object |  |
| `meta.alertKeys` | array<string> |  |
| `meta.endDateInclusive` | string |  |
| `meta.organizationId` | string |  |
| `meta.queryStartTimestamp` | number |  |
| `meta.startDateInclusive` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/alert-full-scan-search` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alert-full-scans.md) for the provider-specific parameters and requirements.

