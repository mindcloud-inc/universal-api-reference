# Zoho Billing: Get Organization



```
GET https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/get-organization
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Billing `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/get-organization?connectionId=$CONNECTION_ID&organizationId=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "organizationId": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoBilling/latest/actions/get-organization?${params}`, {
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
| `organizationId` | string | yes | Unique identifier of the organization. |

## Response

```json
{
  "success": true,
  "data": [
    {
      "code": 1,
      "message": "string",
      "organization": {
        "address": {
          "city": "string",
          "country": "string"
        },
        "contact_name": "Ava Chen",
        "currency_code": "string",
        "custom_fields": [
          [
            {}
          ]
        ],
        "email": "ava@example.com",
        "is_portal_enabled": true,
        "mode": "string",
        "name": "Ava Chen",
        "organization_id": "string",
        "time_zone": "string",
        "version": "string"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `code` | number |  |
| `message` | string |  |
| `organization` | object |  |
| `organization.address` | object |  |
| `organization.address.city` | string |  |
| `organization.address.country` | string |  |
| `organization.contact_name` | string |  |
| `organization.currency_code` | string |  |
| `organization.custom_fields[]` | array<object> |  |
| `organization.email` | string |  |
| `organization.is_portal_enabled` | boolean |  |
| `organization.mode` | string |  |
| `organization.name` | string |  |
| `organization.organization_id` | string |  |
| `organization.time_zone` | string |  |
| `organization.version` | string |  |

## Native endpoint

Through the native Zoho Billing API, this operation is `GET /organizations/:organization_id` (base URL `{{credentials.accessTokenRequest.api_domain}}/billing/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-organization.md) for the provider-specific parameters and requirements.

