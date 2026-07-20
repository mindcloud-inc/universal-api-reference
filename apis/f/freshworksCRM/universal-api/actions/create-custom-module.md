# Freshworks CRM: Create Custom Module

Creates a custom module in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-custom-module
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-custom-module" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "moduleCustomization": {},
  "moduleCustomization.entity_name": "Ava Chen",
  "moduleCustomization.icon": "string",
  "moduleCustomization.plural_name": "Ava Chen",
  "moduleCustomization.singular_name": "Ava Chen"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-custom-module', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "moduleCustomization": {},
    "moduleCustomization.entity_name": "Ava Chen",
    "moduleCustomization.icon": "string",
    "moduleCustomization.plural_name": "Ava Chen",
    "moduleCustomization.singular_name": "Ava Chen"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `moduleCustomization` | object | yes |  |
| `moduleCustomization.description` | string | no |  |
| `moduleCustomization.entity_name` | string | yes |  |
| `moduleCustomization.icon` | string | yes |  |
| `moduleCustomization.plural_name` | string | yes |  |
| `moduleCustomization.show_in_navigation_menu` | boolean | no |  |
| `moduleCustomization.singular_name` | string | yes |  |

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

Through the native Freshworks CRM API, this operation is `POST /api/settings/module_customizations` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-module.md) for the provider-specific parameters and requirements.

