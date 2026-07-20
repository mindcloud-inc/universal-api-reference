# Search for Business ID with GatherUp

Finds a business ID in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/business/search`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Search for Business ID](https://app.gatherup.com/api/doc/business/search)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `by` | body | `string` | yes | Search by... Possible values: customField , extraField |
| `search` | body | `string` | yes | Search value |
