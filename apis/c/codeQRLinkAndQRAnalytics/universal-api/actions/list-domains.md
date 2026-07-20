# CodeQR - Link and QR Analytics: List Domains

Retrieves domains from CodeQR.

```
GET https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a CodeQR - Link and QR Analytics `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-domains?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/codeQRLinkAndQRAnalytics/latest/actions/list-domains?${params}`, {
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
| `search` | string | no | The search term to filter the domains by. |
| `archived` | boolean | no | Whether to include archived domains in the response. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "2026-05-07T12:00:00.000Z",
      "expiredUrl": "https://example.com",
      "id": "string",
      "placeholder": "string",
      "primary": true,
      "slug": "string",
      "target": "string",
      "type": "string",
      "updatedAt": "2026-05-07T12:00:00.000Z",
      "verified": true
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `archived` | boolean |  |
| `createdAt` | date |  |
| `expiredUrl` | string |  |
| `id` | string |  |
| `placeholder` | string |  |
| `primary` | boolean |  |
| `slug` | string |  |
| `target` | string |  |
| `type` | string |  |
| `updatedAt` | date |  |
| `verified` | boolean |  |

## Native endpoint

Through the native CodeQR - Link and QR Analytics API, this operation is `GET /domains` (base URL `https://api.codeqr.io`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

