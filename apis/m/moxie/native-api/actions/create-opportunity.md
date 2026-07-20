# Create Opportunity with Moxie

Creates a new opportunity in Moxie.

## Endpoint

- **Method:** `POST`
- **Path:** `/action/opportunities/create`
- **Base URL:** `https://pod01.withmoxie.com/api/public`
- **Official documentation:** [Create Opportunity](https://help.withmoxie.com/en/articles/8160471-create-opportunity)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Opportunity name. |
| `description` | body | `string` | no | Opportunity description. |
| `clientName` | body | `string` | no | Existing client name for the opportunity. |
| `stageName` | body | `string` | no | Pipeline stage name. |
| `value` | body | `number` | no | Opportunity value. |
| `estCloseDate` | body | `string` | no | Estimated close date in YYYY-MM-DD format. |
| `leadInfo` | body | `object` | no | Lead info object for a new opportunity. |
| `toDos` | body | `list<object>` | no | List of opportunity to-do items. |
| `customValues` | body | `object` | no | Custom values object for the opportunity. |
