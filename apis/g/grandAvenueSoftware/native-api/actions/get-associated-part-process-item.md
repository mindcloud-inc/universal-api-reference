# Get Associated Part related Process Item with Grand Avenue Software

Retrieves an associated part's related process item from Grand Avenue Software.

## Endpoint

- **Method:** `GET`
- **Path:** `/AssociatedParts/:id/ProcessItem`
- **Base URL:** `{baseUrl}`
- **API:** REST

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `$select` | query | `list<string>` | no | Send multiple values as a string. |
| `id` | path | `string` | yes | — |
