# Release0: List Domains

Retrieves custom domains from a Release0 workspace.

```
GET https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-domains
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Release0 `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-domains?connectionId=$CONNECTION_ID&workspaceId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "workspaceId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/release0/latest/actions/list-domains?${params}`, {
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
| `workspaceId` | string | yes | The workspace ID to list domains for. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "archived": true,
      "createdAt": "string",
      "expiredUrl": "https://example.com",
      "id": "string",
      "logo": "string",
      "notFoundUrl": "https://example.com",
      "placeholder": "string",
      "primary": true,
      "slug": "string",
      "updatedAt": "string",
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
| `createdAt` | string |  |
| `expiredUrl` | string |  |
| `id` | string |  |
| `logo` | string |  |
| `notFoundUrl` | string |  |
| `placeholder` | string |  |
| `primary` | boolean |  |
| `slug` | string |  |
| `updatedAt` | string |  |
| `verified` | boolean |  |

## Native endpoint

Through the native Release0 API, this operation is `GET /v1/domains` (base URL `https://release0.com/api`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-domains.md) for the provider-specific parameters and requirements.

