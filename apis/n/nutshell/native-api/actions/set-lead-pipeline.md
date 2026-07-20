# Set Lead Pipeline with Nutshell

Updates a lead's pipeline in Nutshell.

## Endpoint

- **Method:** `POST`
- **Path:** `/leads/:id/stageset`
- **Base URL:** `https://app.nutshell.com/rest`
- **Official documentation:** [Set Lead Pipeline](https://developers.nutshell.com/reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Nutshell lead ID to move. |
| `stageset` | body | `string` | no | The pipeline stageset ID to assign to the lead. |
