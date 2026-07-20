# Freshworks CRM: List Custom Module Fields

Retrieves custom module fields from Freshworks CRM.

```
GET https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-custom-module-fields
```

Authenticate with `Authorization: Bearer $MINDCLOUD_API_KEY` and pass a Freshworks CRM `connectionId` ([setup](../authentication.md)).

## Example request

```bash
curl -X GET "https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-custom-module-fields?connectionId=$CONNECTION_ID&entityType=string" \
  -H "Authorization: Bearer $MINDCLOUD_API_KEY"
```

```js
const params = new URLSearchParams({
  connectionId,
  "entityType": "string"
});

const response = await fetch(`https://connect.mindcloud.co/v1/universal/freshworksCRM/latest/actions/list-custom-module-fields?${params}`, {
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
| `entityType` | string | yes |  |

## Response

```json
{
  "success": true,
  "data": [
    {
      "forms": [
        {
          "active": true,
          "description": "string",
          "fieldClass": "string",
          "fields": [
            {
              "allowClearingDefaultValue": true,
              "choices": [
                {
                  "disabled": true,
                  "id": 1,
                  "inactive": true,
                  "isActive": true,
                  "position": 1,
                  "value": "string"
                }
              ],
              "custom": true,
              "defaultValue": "string",
              "editable": true,
              "fieldClass": "string",
              "fieldOptions": {
                "allowFieldsToBeAdded": true,
                "allowSortInFilter": true,
                "canChoicesBeCustomized": true,
                "canEditableBeChanged": true,
                "canEditableBeChangedFieldPermission": true,
                "canLabelBeRenamed": true,
                "canNotBeHidden": true,
                "canRequiredBeChanged": true,
                "canUniquenessBeChanged": true,
                "defaultDisplayLabel": "string",
                "lookupPrefetchUrl": "https://example.com",
                "lookupType": "string",
                "systemField": true
              },
              "fields": [
                {
                  "allowClearingDefaultValue": true,
                  "choices": [
                    {
                      "disabled": true,
                      "id": 1,
                      "inactive": true,
                      "isActive": true,
                      "position": 1,
                      "value": "string"
                    }
                  ],
                  "custom": true,
                  "defaultValue": "string",
                  "editable": true,
                  "fieldClass": "string",
                  "fieldOptions": {
                    "allowFieldsToBeAdded": true,
                    "allowSortInFilter": true,
                    "canChoicesBeCustomized": true,
                    "canEditableBeChanged": true,
                    "canEditableBeChangedFieldPermission": true,
                    "canLabelBeRenamed": true,
                    "canNotBeHidden": true,
                    "canRequiredBeChanged": true,
                    "canUniquenessBeChanged": true,
                    "defaultDisplayLabel": "string",
                    "lookupPrefetchUrl": "https://example.com",
                    "lookupType": "string",
                    "systemField": true
                  },
                  "formId": 1,
                  "hint": "string",
                  "id": "string",
                  "label": "string",
                  "link": "https://example.com",
                  "name": "Ava Chen",
                  "originalLabel": "string",
                  "originalPlaceholder": "string",
                  "parentId": "string",
                  "placeholder": "string",
                  "position": 1,
                  "quickAddPosition": 1,
                  "required": true,
                  "type": "string",
                  "visible": true
                }
              ],
              "formId": 1,
              "hint": "string",
              "id": "string",
              "label": "string",
              "link": "https://example.com",
              "name": "Ava Chen",
              "originalLabel": "string",
              "originalPlaceholder": "string",
              "parentId": "string",
              "placeholder": "string",
              "position": 1,
              "quickAddPosition": 1,
              "required": true,
              "type": "string",
              "visible": true
            }
          ],
          "formClass": "string",
          "groupedMandatoryFields": [
            {}
          ],
          "id": 1,
          "name": "Ava Chen"
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
| `forms` | array<object> |  |
| `forms[].active` | boolean |  |
| `forms[].description` | string |  |
| `forms[].fieldClass` | string |  |
| `forms[].fields` | array<object> |  |
| `forms[].fields[].allowClearingDefaultValue` | boolean |  |
| `forms[].fields[].choices` | array<object> |  |
| `forms[].fields[].choices[].disabled` | boolean |  |
| `forms[].fields[].choices[].id` | number |  |
| `forms[].fields[].choices[].inactive` | boolean |  |
| `forms[].fields[].choices[].isActive` | boolean |  |
| `forms[].fields[].choices[].position` | number |  |
| `forms[].fields[].choices[].value` | string |  |
| `forms[].fields[].custom` | boolean |  |
| `forms[].fields[].defaultValue` | string |  |
| `forms[].fields[].editable` | boolean |  |
| `forms[].fields[].fieldClass` | string |  |
| `forms[].fields[].fieldOptions` | object |  |
| `forms[].fields[].fieldOptions.allowFieldsToBeAdded` | boolean |  |
| `forms[].fields[].fieldOptions.allowSortInFilter` | boolean |  |
| `forms[].fields[].fieldOptions.canChoicesBeCustomized` | boolean |  |
| `forms[].fields[].fieldOptions.canEditableBeChanged` | boolean |  |
| `forms[].fields[].fieldOptions.canEditableBeChangedFieldPermission` | boolean |  |
| `forms[].fields[].fieldOptions.canLabelBeRenamed` | boolean |  |
| `forms[].fields[].fieldOptions.canNotBeHidden` | boolean |  |
| `forms[].fields[].fieldOptions.canRequiredBeChanged` | boolean |  |
| `forms[].fields[].fieldOptions.canUniquenessBeChanged` | boolean |  |
| `forms[].fields[].fieldOptions.defaultDisplayLabel` | string |  |
| `forms[].fields[].fieldOptions.lookupPrefetchUrl` | string |  |
| `forms[].fields[].fieldOptions.lookupType` | string |  |
| `forms[].fields[].fieldOptions.systemField` | boolean |  |
| `forms[].fields[].fields` | array<object> |  |
| `forms[].fields[].fields[].allowClearingDefaultValue` | boolean |  |
| `forms[].fields[].fields[].choices` | array<object> |  |
| `forms[].fields[].fields[].choices[].disabled` | boolean |  |
| `forms[].fields[].fields[].choices[].id` | number |  |
| `forms[].fields[].fields[].choices[].inactive` | boolean |  |
| `forms[].fields[].fields[].choices[].isActive` | boolean |  |
| `forms[].fields[].fields[].choices[].position` | number |  |
| `forms[].fields[].fields[].choices[].value` | string |  |
| `forms[].fields[].fields[].custom` | boolean |  |
| `forms[].fields[].fields[].defaultValue` | string |  |
| `forms[].fields[].fields[].editable` | boolean |  |
| `forms[].fields[].fields[].fieldClass` | string |  |
| `forms[].fields[].fields[].fieldOptions` | object |  |
| `forms[].fields[].fields[].fieldOptions.allowFieldsToBeAdded` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.allowSortInFilter` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.canChoicesBeCustomized` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.canEditableBeChanged` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.canEditableBeChangedFieldPermission` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.canLabelBeRenamed` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.canNotBeHidden` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.canRequiredBeChanged` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.canUniquenessBeChanged` | boolean |  |
| `forms[].fields[].fields[].fieldOptions.defaultDisplayLabel` | string |  |
| `forms[].fields[].fields[].fieldOptions.lookupPrefetchUrl` | string |  |
| `forms[].fields[].fields[].fieldOptions.lookupType` | string |  |
| `forms[].fields[].fields[].fieldOptions.systemField` | boolean |  |
| `forms[].fields[].fields[].formId` | number |  |
| `forms[].fields[].fields[].hint` | string |  |
| `forms[].fields[].fields[].id` | string |  |
| `forms[].fields[].fields[].label` | string |  |
| `forms[].fields[].fields[].link` | string |  |
| `forms[].fields[].fields[].name` | string |  |
| `forms[].fields[].fields[].originalLabel` | string |  |
| `forms[].fields[].fields[].originalPlaceholder` | string |  |
| `forms[].fields[].fields[].parentId` | string |  |
| `forms[].fields[].fields[].placeholder` | string |  |
| `forms[].fields[].fields[].position` | number |  |
| `forms[].fields[].fields[].quickAddPosition` | number |  |
| `forms[].fields[].fields[].required` | boolean |  |
| `forms[].fields[].fields[].type` | string |  |
| `forms[].fields[].fields[].visible` | boolean |  |
| `forms[].fields[].formId` | number |  |
| `forms[].fields[].hint` | string |  |
| `forms[].fields[].id` | string |  |
| `forms[].fields[].label` | string |  |
| `forms[].fields[].link` | string |  |
| `forms[].fields[].name` | string |  |
| `forms[].fields[].originalLabel` | string |  |
| `forms[].fields[].originalPlaceholder` | string |  |
| `forms[].fields[].parentId` | string |  |
| `forms[].fields[].placeholder` | string |  |
| `forms[].fields[].position` | number |  |
| `forms[].fields[].quickAddPosition` | number |  |
| `forms[].fields[].required` | boolean |  |
| `forms[].fields[].type` | string |  |
| `forms[].fields[].visible` | boolean |  |
| `forms[].formClass` | string |  |
| `forms[].groupedMandatoryFields` | array<object> |  |
| `forms[].id` | number |  |
| `forms[].name` | string |  |

## Native endpoint

Through the native Freshworks CRM API, this operation is `GET /api/settings/:entity_type/forms` (base URL `https://{{credentials.bundleAlias}}`). The Universal API call above is translated to it by MindCloud, including authentication. See the [native action reference](../../native-api/actions/list-custom-module-fields.md) for the provider-specific parameters and requirements.

