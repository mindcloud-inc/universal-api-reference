# Create Object Schema with HubSpot

Creates a new object schema in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm-object-schemas/v3/schemas`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Query Pagination
- **Official documentation:** [Create Object Schema](https://developers.hubspot.com/docs/api-reference/crm-schemas-v3/core/post-crm-object-schemas-v3-schemas)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Internal singular name for the custom object schema. |
| `labels` | body | `object` | yes | Singular and plural display labels for the custom object. |
| `labels.singular` | body | `string` | yes | Singular display label for the custom object. |
| `labels.plural` | body | `string` | yes | Plural display label for the custom object. |
| `description` | body | `string` | no | Optional description for the schema. |
| `primaryDisplayProperty` | body | `string` | no | Property name used as the primary display label. |
| `searchableProperties[]` | body | `array<string>` | no | Property names that should be searchable. |
| `secondaryDisplayProperties[]` | body | `array<string>` | no | Property names shown as secondary display fields. |
| `requiredProperties[]` | body | `array<string>` | no | Property names HubSpot should require on records. |
| `associatedObjects[]` | body | `array<string>` | no | HubSpot standard objects that can associate with this custom object. |
| `properties[]` | body | `array<object>` | no | Property definitions to create with the schema. |
| `properties[].name` | body | `string` | no | Internal name for a custom property. |
| `properties[].label` | body | `string` | no | Display label for a custom property. |
| `properties[].type` | body | `string` | no | HubSpot data type for the property. Accepted values: `date`, `datetime`, `enumeration`, `number`, `string`. |
| `properties[].fieldType` | body | `string` | no | HubSpot field type for the property. Accepted values: `booleancheckbox`, `checkbox`, `date`, `file`, `number`, `radio`, `select`, `text`, `textarea`. |
| `properties[].groupName` | body | `string` | no | Group name for the custom property. |
| `properties[].hasUniqueValue` | body | `boolean` | no | Whether HubSpot should enforce unique values for the property. |
| `properties[].isPrimaryDisplayLabel` | body | `boolean` | no | Whether this property should be used as the primary display label. |
| `properties[].options[]` | body | `array<object>` | no | Enumeration options for the property. |
| `properties[].options[].label` | body | `string` | no | Display label for an enumeration option. |
| `properties[].options[].value` | body | `string` | no | Stored value for an enumeration option. |
