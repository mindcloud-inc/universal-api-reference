# DNSFilter: Get Block Page



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-block-page
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-block-page?connectionId=$CONNECTION_ID&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-block-page?${params}`, {
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
| `id` | number | yes | Block page ID |

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

Through the native DNSFilter API, this operation is `GET /v1/block_pages/:id` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-block-page.md) for the provider-specific parameters and requirements.

