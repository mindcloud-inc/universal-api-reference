# Zoho Inventory: List Organizations

Retrieves organizations from Zoho Inventory.

```
GET https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-organizations
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Zoho Inventory `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-organizations?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/zohoInventory/latest/actions/list-organizations?${params}`, {
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
      "country": "string",
      "country_code": "string",
      "currency_code": "string",
      "email": "ava@example.com",
      "is_default_org": true,
      "is_org_active": true,
      "name": "Ava Chen",
      "org_joined_app_list": [
        "string"
      ],
      "organization_id": "string",
      "time_zone": "string"
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `country` | string |  |
| `country_code` | string |  |
| `currency_code` | string |  |
| `email` | string |  |
| `is_default_org` | boolean |  |
| `is_org_active` | boolean |  |
| `name` | string |  |
| `org_joined_app_list` | array<string> |  |
| `organization_id` | string |  |
| `time_zone` | string |  |

## Native endpoint

Through the native Zoho Inventory API, this operation is `GET /organizations` (base URL `{{credentials.accessTokenRequest.api_domain}}/inventory/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-organizations.md) for the provider-specific parameters and requirements.

