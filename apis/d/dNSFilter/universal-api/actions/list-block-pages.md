# DNSFilter: List Block Pages



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-block-pages
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

This action also supports [pagination](../pagination.md) (`limit`, `offset`).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-block-pages?connectionId=$CONNECTION_ID&limit=25&offset=0" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  limit: '25',
  offset: '0'
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/list-block-pages?${params}`, {
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
| `organizationId` | number | no | Organization ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "block_email_addr": "ava@example.com",
      "block_logo_uuid": "string",
      "block_org_name": "Ava Chen",
      "created_at": "2026-05-07T12:00:00.000Z",
      "name": "Ava Chen",
      "organization_id": 1,
      "updated_at": "2026-05-07T12:00:00.000Z"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `block_email_addr` | string |  |
| `block_logo_uuid` | string |  |
| `block_org_name` | string |  |
| `created_at` | date |  |
| `name` | string |  |
| `organization_id` | number |  |
| `updated_at` | date |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/block_pages` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication and pagination. See the [native action reference](../../native-api/actions/list-block-pages.md) for the provider-specific parameters and requirements.

