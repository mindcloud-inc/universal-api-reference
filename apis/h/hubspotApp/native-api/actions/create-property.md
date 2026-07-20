# Create Property with HubSpot

Creates a new property in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/properties/:objectType`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Property](https://developers.hubspot.com/docs/api-reference/crm-properties-v3/core/post-crm-v3-properties-objectType)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `objectType` | path | `string` | yes | The HubSpot object type that will own the property, such as contacts, companies, deals, tickets, products, or a custom object type. |
| `groupName` | body | `string` | yes | The existing HubSpot property group that will contain the property. |
| `name` | body | `string` | yes | The internal property name, for example favorite_food. |
| `label` | body | `string` | yes | The display label shown in HubSpot. |
| `type` | body | `list` | yes | The HubSpot data type for the property. Accepted values: `bool`, `date`, `datetime`, `enumeration`, `number`, `string`. |
| `fieldType` | body | `list` | yes | How the property should be rendered in HubSpot. Accepted values: `booleancheckbox`, `calculation_equation`, `checkbox`, `date`, `file`, `html`, `number`, `phonenumber`, `radio`, `select`, `text`, `textarea`. |
| `description` | body | `string` | no | Optional description for the property. |
| `hasUniqueValue` | body | `boolean` | no | Whether HubSpot should enforce unique values for the property. |
| `options[]` | body | `array<object>` | no | Enumeration options for the property. |
| `options[].label` | body | `string` | no | Display label for an enumeration option. |
| `options[].value` | body | `string` | no | Stored value for an enumeration option. |
| `calculationFormula` | body | `string` | no | Formula used when creating a calculation property. |
| `externalOptions` | body | `boolean` | no | Whether the property options should be populated dynamically from HubSpot instead of a static option list. |
| `referencedObjectType` | body | `list` | no | The HubSpot object type that provides external option values. Use OWNER for HubSpot user-picker fields. Accepted values: `OWNER`. |
| `formField` | body | `boolean` | no | Whether the property can be used on HubSpot forms. |
| `displayOrder` | body | `number` | no | Display order within the property group. HubSpot places -1 after positive values. |
| `hidden` | body | `boolean` | no | Whether the property should be hidden in HubSpot. |
| `dataSensitivity` | body | `list` | no | Sensitivity classification for the property. Accepted values: `highly_sensitive`, `non_sensitive`, `sensitive`. |
