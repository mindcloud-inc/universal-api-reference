# Freshworks CRM: Get Custom Module

Retrieves a custom module from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-custom-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-custom-module?connectionId=$CONNECTION_ID&id=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "id": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/get-custom-module?${params}`, {
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
| `id` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "module_customization": {
        "coll_id": "string",
        "configs": {
          "filters_v2_enabled": true
        },
        "created_at": "2026-05-07T12:00:00.000Z",
        "custom": true,
        "description": "string",
        "entity_name": "Ava Chen",
        "icon": "string",
        "id": 1,
        "layout_customizations": {
          "lookup_sections": [
            "string"
          ],
          "section_config": [
            "string"
          ]
        },
        "plural_name": "Ava Chen",
        "position": 1,
        "renaming_customizations": {},
        "resource_path_for_navigation": "string",
        "show_in_navigation_menu": true,
        "singular_name": "Ava Chen",
        "status": 1,
        "table_name": "Ava Chen",
        "updated_at": "2026-05-07T12:00:00.000Z"
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `module_customization.coll_id` | string |  |
| `module_customization.configs.filters_v2_enabled` | boolean |  |
| `module_customization.created_at` | date |  |
| `module_customization.custom` | boolean |  |
| `module_customization.description` | string |  |
| `module_customization.entity_name` | string |  |
| `module_customization.icon` | string |  |
| `module_customization.id` | number |  |
| `module_customization.layout_customizations.lookup_sections` | array |  |
| `module_customization.layout_customizations.section_config` | array |  |
| `module_customization.plural_name` | string |  |
| `module_customization.position` | number |  |
| `module_customization.renaming_customizations` | object |  |
| `module_customization.resource_path_for_navigation` | string |  |
| `module_customization.show_in_navigation_menu` | boolean |  |
| `module_customization.singular_name` | string |  |
| `module_customization.status` | number |  |
| `module_customization.table_name` | string |  |
| `module_customization.updated_at` | date |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET /api/settings/module_customizations/:id` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/get-custom-module.md) for the provider-specific parameters and requirements.

