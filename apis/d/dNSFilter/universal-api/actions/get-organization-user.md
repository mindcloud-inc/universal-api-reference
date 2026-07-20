# DNSFilter: Get Organization User



```
GET https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-organization-user
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a DNSFilter `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-organization-user?connectionId=$CONNECTION_ID&organizationId=1&id=1" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "1",
  "id": "1"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/dNSFilter/latest/actions/get-organization-user?${params}`, {
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
| `organizationId` | number | yes | Organization ID |
| `id` | number | yes | User ID |

## Response

```json
{
  "success": true,
  "data": [
    {
      "created_at": "2026-05-07T12:00:00.000Z",
      "email": "ava@example.com",
      "email_verified": true,
      "id": 1,
      "name": "Ava Chen",
      "role": "string",
      "updated_at": "2026-05-07T12:00:00.000Z",
      "uuid": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `created_at` | date |  |
| `email` | string |  |
| `email_verified` | boolean |  |
| `id` | number |  |
| `name` | string |  |
| `role` | string |  |
| `updated_at` | date |  |
| `uuid` | string |  |

## Native endpoint

Through the native DNSFilter API, this operation is `GET /v1/organizations/:organization_id/users/:id` (base URL `https://api.dnsfilter.com`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization-user.md) for the provider-specific parameters and requirements.

