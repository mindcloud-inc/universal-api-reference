# List Locale Groups with Woztell

Retrieves locale groups from your Woztell workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/`
- **Base URL:** `https://open.api.woztell.com/v3`
- **Official documentation:** [List Locale Groups](https://doc.woztell.com/docs/reference/open-api-reference/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables` | body | `object` | no | Optional GraphQL variables object. Supported keys include localeGroupIds, first, last, after, before, search, and sortBy. |
