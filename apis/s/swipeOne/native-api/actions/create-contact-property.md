# Create Contact Property with Swipe One

## Endpoint

- **Method:** `POST`
- **Path:** `/workspaces/:workspaceId/contact-properties`
- **Base URL:** `https://api.swipeone.com/api`
- **Official documentation:** [Create Contact Property](https://docs.swipeone.com/en/articles/10540803-contact-properties#h_b218be703a)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workspaceId` | path | `string` | yes | Unique identifier of the workspace where the contact property will be created. |
| `label` | body | `string` | yes | The human-readable label for the contact property. |
| `name` | body | `string` | no | The unique name of the contact property. |
| `fieldType` | body | `string` | yes | The field type for the contact property. |
| `numberFormat` | body | `string` | no | Number format when field type is number. |
| `currency` | body | `string` | no | Currency code when number format is currency. |
| `dateFormat` | body | `string` | no | Date format when field type is date. |
| `includeTime` | body | `boolean` | no | Whether to include time when field type is date. |
| `addressFields` | body | `object` | no | Address field configuration when field type is address. |
| `options` | body | `list<object>` | no | Selectable options when field type is select or multiselect. |
| `optionsName` | body | `string` | no | Optional group name for selectable options. |
