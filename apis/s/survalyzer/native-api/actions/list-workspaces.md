# List Workspaces with Survalyzer

## Endpoint

- **Method:** `POST`
- **Path:** `/publicapi/Survey/v3/ReadWorkspaceList`
- **Base URL:** `https://api.survalyzer-eu.app`
- **Official documentation:** [List Workspaces](https://developer.survalyzer.com/knowledge-base/public-api-eu/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `conditionOperator` | body | `string` | no | Comparison operator used by the provider filter. |
| `conditionType` | body | `string` | no | Provider filter object type to search. |
| `conjunction` | body | `string` | no | How multiple filters should be combined. |
| `identifier` | body | `string` | no | Field identifier used in the filter. |
| `page` | body | `string` | no | 1-based results page number. |
| `pageSize` | body | `string` | no | Maximum number of records to return. |
| `value` | body | `string` | no | Filter comparison value. |
