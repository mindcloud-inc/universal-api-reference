# List Opt-Outs with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Distribute/v3/ReadOptOutList`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [List Opt-Outs](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditionOperator` | body | `string` | no | Comparison operator used by the provider filter. |
| `conditionType` | body | `string` | no | Provider filter object type to search. |
| `conjunction` | body | `string` | no | How multiple filters should be combined. |
| `identifier` | body | `string` | no | Field identifier used in the filter. |
| `page` | body | `string` | no | 1-based results page number. |
| `pageSize` | body | `string` | no | Maximum number of records to return. |
| `panelId` | body | `string` | no | Optional panel scope for the opt-out list. |
| `value` | body | `string` | no | Filter comparison value. |
| `workspaceId` | body | `string` | no | Workspace scope for the opt-out list. |
