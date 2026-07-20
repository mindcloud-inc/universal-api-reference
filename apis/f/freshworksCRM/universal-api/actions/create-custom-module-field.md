# Freshworks CRM: Create Custom Module Field

Creates a custom module field in Freshworks CRM.

```
POST https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-custom-module-field
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X POST "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-custom-module-field" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY" \
  -H "Content-Type: application/json" \
  -d '{
  "connectionId": "$CONNECTION_ID",
  "entityType": "string",
  "fieldType": 1,
  "formId": "string",
  "label": "string"
}'
```

```js
const response = await fetch('https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/create-custom-module-field', {
  method: 'POST',
  headers: {
    Authorization: `Bearer ${process.env.MINDCLOUD_API_KEY}`,
    'Content-Type': 'application/json'
  },
  body: JSON.stringify({
    connectionId,
    "entityType": "string",
    "fieldType": 1,
    "formId": "string",
    "label": "string"
  })
});

const { success, data } = await response.json();
```

## Inputs

Arguments are sent as JSON body fields ([conventions](../arguments.md)).

| Key | Type | Required | Description |
| --- | --- | --- | --- |
| `entityType` | string | yes |  |
| `fieldType` | number | yes |  |
| `formId` | string | yes |  |
| `label` | string | yes |  |
| `required` | boolean | no |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "field": {
        "allow_clearing_default_value": true,
        "choices": [
          "string"
        ],
        "custom": true,
        "default_value": "string",
        "editable": true,
        "field_class": "string",
        "field_options": {
          "allow_fields_to_be_added": true,
          "can_choices_be_customized": true,
          "can_editable_be_changed": true,
          "can_editable_be_changed_field_permission": true,
          "can_label_be_renamed": true,
          "can_not_be_hidden": true,
          "can_required_be_changed": true,
          "can_uniqueness_be_changed": true,
          "system_field": true,
          "unique": "string"
        },
        "fields": [
          "string"
        ],
        "form_id": 1,
        "hint": "string",
        "id": "string",
        "label": "string",
        "link": "https://example.com",
        "name": "Ava Chen",
        "parent_id": "string",
        "placeholder": "string",
        "position": 1,
        "quick_add_position": 1,
        "required": true,
        "type": "string",
        "visible": true
      }
    }
  ],
  "meta": {}
}
```

### Response fields

| Key | Type | Description |
| --- | --- | --- |
| `field.allow_clearing_default_value` | boolean |  |
| `field.choices` | array |  |
| `field.custom` | boolean |  |
| `field.default_value` | string |  |
| `field.editable` | boolean |  |
| `field.field_class` | string |  |
| `field.field_options.allow_fields_to_be_added` | boolean |  |
| `field.field_options.can_choices_be_customized` | boolean |  |
| `field.field_options.can_editable_be_changed` | boolean |  |
| `field.field_options.can_editable_be_changed_field_permission` | boolean |  |
| `field.field_options.can_label_be_renamed` | boolean |  |
| `field.field_options.can_not_be_hidden` | boolean |  |
| `field.field_options.can_required_be_changed` | boolean |  |
| `field.field_options.can_uniqueness_be_changed` | boolean |  |
| `field.field_options.system_field` | boolean |  |
| `field.field_options.unique` | string |  |
| `field.fields` | array |  |
| `field.form_id` | number |  |
| `field.hint` | string |  |
| `field.id` | string |  |
| `field.label` | string |  |
| `field.link` | string |  |
| `field.name` | string |  |
| `field.parent_id` | string |  |
| `field.placeholder` | string |  |
| `field.position` | number |  |
| `field.quick_add_position` | number |  |
| `field.required` | boolean |  |
| `field.type` | string |  |
| `field.visible` | boolean |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `POST /api/settings/:entity_type/forms/:form_id/fields` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/create-custom-module-field.md) for the provider-specific parameters and requirements.

