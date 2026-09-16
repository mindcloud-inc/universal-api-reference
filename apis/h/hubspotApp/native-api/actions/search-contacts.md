# Search Contacts with HubSpot

Finds contacts in HubSpot.

## Endpoint

- **Method:** `POST`
- **Path:** `crm/v3/objects/contacts/search`
- **Base URL:** `https://api.hubapi.com`
- **API:** REST - Body Pagination
- **Official documentation:** [Search Contacts](https://developers.hubspot.com/docs/api-reference/crm-contacts-v3/search/post-crm-v3-objects-contacts-search)

## Capabilities

This operation supports [pagination](../README.md#pagination), [filtering](../README.md#filtering), and [sorting](../README.md#sorting).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `query` | body | `string` | no | The text to search across default searchable contact properties. |
| `emailContains` | body | `string` | no | Filter contacts whose email contains this value. For a domain, enter @mindcloud.co; the action sends HubSpot an email CONTAINS_TOKEN filter with the correct wildcard format. |
| `filterPropertyName` | body | `list<string>` | no | Choose any contact property to filter search results by. |
| `filterOperator` | body | `list` | no | Choose how to compare the selected contact property to the filter value. Accepted values: `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`. |
| `filterValue` | body | `string` | no | Enter the value to search for in the selected contact property. |
| `properties` | body | `list<string>` | no | Select the contact properties to include in the response. Send multiple values as a array. |
| `filterGroups[].filters[]` | body | `array<object>` | no | Raw HubSpot filter group filters for advanced searches. Use these when you need multiple filters, AND/OR groups, IN/NOT_IN, or BETWEEN filtering. |
| `filterGroups[].filters[].propertyName` | body | `list<string>` | no | The HubSpot contact property name for an advanced raw filter. |
| `filterGroups[].filters[].operator` | body | `list` | no | The HubSpot search operator for an advanced raw filter. Accepted values: `BETWEEN`, `CONTAINS_TOKEN`, `EQ`, `GT`, `GTE`, `HAS_PROPERTY`, `IN`, `LT`, `LTE`, `NEQ`, `NOT_CONTAINS_TOKEN`, `NOT_HAS_PROPERTY`, `NOT_IN`. |
| `filterGroups[].filters[].value` | body | `string` | no | The primary comparison value for an advanced raw filter. Required for operators such as EQ, CONTAINS_TOKEN, and the lower bound of BETWEEN. |
| `filterGroups[].filters[].values[]` | body | `array<string>` | no | Multiple values for IN or NOT_IN advanced filters. |
| `filterGroups[].filters[].highValue` | body | `string` | no | The upper bound for BETWEEN advanced filters. |
