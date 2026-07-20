# Socket: Get Threat Feed Items for Organization

Retrieves organization threat feed items from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-threat-feed-items-for-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-threat-feed-items-for-organization?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/get-threat-feed-items-for-organization?${params}`, {
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`
  }
});

const { success, data } = await response.json();
```



## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPageCursor": "string",
      "results": [
        {
          "createdAt": "2026-05-07T12:00:00.000Z",
          "description": "string",
          "id": 1,
          "locationHtmlUrl": "https://example.com",
          "needsHumanReview": true,
          "packageHtmlUrl": "https://example.com",
          "publishedAt": "2026-05-07T12:00:00.000Z",
          "purl": "https://example.com",
          "removedAt": "2026-05-07T12:00:00.000Z",
          "threatInstanceId": 1,
          "threatType": "string",
          "updatedAt": "2026-05-07T12:00:00.000Z"
        }
      ]
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `nextPageCursor` | string |  |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].createdAt` | date | ISO 8601 timestamp of when the threat in the package artifact was first discovered |
| `results[].description` | string | Detailed description of the underlying threat |
| `results[].id` | number | Unique identifier of the threat feed entry |
| `results[].locationHtmlUrl` | string | URL to the threat details page on Socket |
| `results[].needsHumanReview` | boolean | Whether the threat still is in need of human review by the threat research team |
| `results[].packageHtmlUrl` | string | URL to the affected package page on Socket |
| `results[].publishedAt` | date | ISO 8601 timestamp of when the package artifact was published to the respective registry |
| `results[].purl` | string | Package URL (PURL) of the affected package artifact |
| `results[].removedAt` | date | ISO 8601 timestamp of when the package artifact was removed from the respective registry, or null if the package is still available on the registry |
| `results[].threatInstanceId` | number | Unique threat instance identifier across artifacts |
| `results[].threatType` | string | Threat classification. Possible values: `malware` (known malware), `possible_malware` (AI-detected potential malware), `vulnerability` (potential vulnerability), `typosquat` (human-reviewed typosquat), `possible_typosquat` (AI-detected potential typosquat), `anomaly` (anomalous behavior), `telemetry` (telemetry), `obfuscated` (obfuscated code), `dual_use` (dual-use tool), `troll` (protestware or joke package), `unreviewed` (not yet reviewed), `false_positive` (confirmed false positive). |
| `results[].updatedAt` | date | ISO 8601 timestamp of when the threat record for the package artifact was last updated (e.g., classification changed, package removed from registry, etc.) |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/threat-feed` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-threat-feed-items-for-organization.md) for the provider-specific parameters and requirements.

