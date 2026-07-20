# Socket: List Diff Scans

Retrieves organization diff scans from Socket.

```
GET https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-diff-scans
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Socket `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-diff-scans?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/socket/latest/actions/list-diff-scans?${params}`, {
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
| `afterFullScanId` | string | no |  |
| `beforeFullScanId` | string | no |  |
| `cursor` | string | no |  |
| `direction` | string | no |  |
| `perPage` | number | no |  |
| `repositoryId` | string | no |  |
| `sort` | string | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "nextCursor": "string",
      "nextPageHref": "string",
      "results": [
        {
          "afterFullScanId": "string",
          "apiUrl": "https://example.com",
          "beforeFullScanId": "string",
          "createdAt": "string",
          "description": "string",
          "externalHref": "string",
          "htmlUrl": "https://example.com",
          "id": "string",
          "merge": true,
          "organizationId": "string",
          "repositoryId": "string",
          "updatedAt": "string"
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
| `nextCursor` | string |  |
| `nextPageHref` | string |  |
| `results` | array<object> |  |
| `results[]` | object |  |
| `results[].afterFullScanId` | string |  |
| `results[].apiUrl` | string |  |
| `results[].beforeFullScanId` | string |  |
| `results[].createdAt` | string |  |
| `results[].description` | string |  |
| `results[].externalHref` | string |  |
| `results[].htmlUrl` | string |  |
| `results[].id` | string |  |
| `results[].merge` | boolean |  |
| `results[].organizationId` | string |  |
| `results[].repositoryId` | string |  |
| `results[].updatedAt` | string |  |

## Native endpoint

Through the native Socket API, this operation is `GET /orgs/:org_slug/diff-scans` (base URL `https://api.socket.dev/v0`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-diff-scans.md) for the provider-specific parameters and requirements.

