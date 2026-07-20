# Socket: List Alert Triage

Retrieves organization alert triage rules from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alert-triage
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alert-triage?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-alert-triage?${params}`, {
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
| `direction` | string | no |  |
| `direction` | string | no |  |
| `page` | number | no |  |
| `page` | number | no |  |
| `perPage` | number | no |  |
| `perPage` | number | no |  |
| `sort` | string | no |  |
| `sort` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextPage": 1,
      "results": [
        {
          "alertKey": "string",
          "alertType": "string",
          "createdAt": "string",
          "cveOrGhsaId": "string",
          "cvssScoreCmp": "string",
          "fixAvailable": "string",
          "kevs": "string",
          "note": "string",
          "organizationId": "string",
          "packageName": "Ava Chen",
          "packageNamespace": "Ava Chen",
          "packageType": "string",
          "packageVersion": "string",
          "patchAvailable": "string",
          "reachability": "string",
          "state": "string",
          "updatedAt": "string",
          "uuid": "string"
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
| `nextPage` | number |  |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].alertKey` | string | The alert_key associated with the triage state |
| `results[].alertType` | string | The alert type (e.g., criticalCVE, highCVE) associated with the triage state |
| `results[].createdAt` | string | The creation date of the triage action |
| `results[].cveOrGhsaId` | string | CVE or GHSA ID associated with the triage state |
| `results[].cvssScoreCmp` | string | CVSS score comparison (e.g., >=7.5, >5.0, ==8.0) |
| `results[].fixAvailable` | string | Whether a fix must be available, unavailable, or * for any |
| `results[].kevs` | string | Whether the alert has a CISA KEV (Known Exploited Vulnerability), can be exist, none, or * for any |
| `results[].note` | string | The note associated with the triage action |
| `results[].organizationId` | string | The organization id associated with the triage action |
| `results[].packageName` | string | The package name associated with the triage state |
| `results[].packageNamespace` | string | The package namespace associated with the triage state |
| `results[].packageType` | string | The package type associated with the triage state |
| `results[].packageVersion` | string | The package version associated with the triage state, it can contain a * suffix for wildcard matching |
| `results[].patchAvailable` | string | Whether a patch must be available, unavailable, or * for any |
| `results[].reachability` | string | The reachability of the alert, can be reachable, unreachable, other, or * for any |
| `results[].state` | string | The triage state of the alert |
| `results[].updatedAt` | string | The last update date of the triage action |
| `results[].uuid` | string | The uuid of the triage action |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/triage/alerts` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-alert-triage.md) for the provider-specific parameters and requirements.

