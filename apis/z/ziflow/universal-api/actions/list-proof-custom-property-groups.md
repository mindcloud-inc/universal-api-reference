# Ziflow: List Proof Custom Property Groups

Retrieves proof custom property groups from Ziflow.

```
GET https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-custom-property-groups
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Ziflow `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-custom-property-groups?connectionId=$CONNECTION_ID" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/ziflow/latest/actions/list-proof-custom-property-groups?${params}`, {
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
      "active": true,
      "created_at": "string",
      "created_by": {
        "blocked": true,
        "company": "string",
        "email": "ava@example.com",
        "first_name": "Ava",
        "id": "string",
        "language": "string",
        "last_name": "Chen",
        "phone": "string",
        "proofing_defaults": {
          "comment": true,
          "decision": true,
          "manage": true,
          "notification": "string",
          "share": true,
          "view": true
        },
        "roles": [
          "string"
        ],
        "tenant": {
          "company_name": "Ava Chen",
          "subdomain": "string",
          "tenant_id": "string"
        },
        "timezone": "string",
        "type": "string",
        "verified": true
      },
      "display_order": 1,
      "id": "string",
      "name": "Ava Chen",
      "properties": [
        {
          "display_order": 1,
          "field_type": {
            "allow_new_values": true,
            "default_color": "string",
            "default_values": "string",
            "include_in_search": true,
            "options": [
              {
                "color": "string",
                "display_order": 1,
                "id": "string",
                "value": "string",
                "visible": true
              }
            ],
            "type": "string"
          },
          "group_id": "string",
          "hint": "string",
          "id": "string",
          "mandatory": true,
          "name": "Ava Chen",
          "visible": true
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
| `active` | boolean |  |
| `created_at` | string |  |
| `created_by.blocked` | boolean |  |
| `created_by.company` | string |  |
| `created_by.email` | string |  |
| `created_by.first_name` | string |  |
| `created_by.id` | string |  |
| `created_by.language` | string |  |
| `created_by.last_name` | string |  |
| `created_by.phone` | string |  |
| `created_by.proofing_defaults.comment` | boolean |  |
| `created_by.proofing_defaults.decision` | boolean |  |
| `created_by.proofing_defaults.manage` | boolean |  |
| `created_by.proofing_defaults.notification` | string |  |
| `created_by.proofing_defaults.share` | boolean |  |
| `created_by.proofing_defaults.view` | boolean |  |
| `created_by.roles[]` | string |  |
| `created_by.tenant.company_name` | string |  |
| `created_by.tenant.subdomain` | string |  |
| `created_by.tenant.tenant_id` | string |  |
| `created_by.timezone` | string |  |
| `created_by.type` | string |  |
| `created_by.verified` | boolean |  |
| `display_order` | number |  |
| `id` | string |  |
| `name` | string |  |
| `properties[].display_order` | number |  |
| `properties[].field_type.allow_new_values` | boolean |  |
| `properties[].field_type.default_color` | string |  |
| `properties[].field_type.default_values` | string |  |
| `properties[].field_type.include_in_search` | boolean |  |
| `properties[].field_type.options[].color` | string |  |
| `properties[].field_type.options[].display_order` | number |  |
| `properties[].field_type.options[].id` | string |  |
| `properties[].field_type.options[].value` | string |  |
| `properties[].field_type.options[].visible` | boolean |  |
| `properties[].field_type.type` | string |  |
| `properties[].group_id` | string |  |
| `properties[].hint` | string |  |
| `properties[].id` | string |  |
| `properties[].mandatory` | boolean |  |
| `properties[].name` | string |  |
| `properties[].visible` | boolean |  |

## Native endpoint

Through the native Ziflow API, this operation is `GET /custom-properties/proofs/groups` (base URL `https://api.ziflow.io/v1`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-proof-custom-property-groups.md) for the provider-specific parameters and requirements.

