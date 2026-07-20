# Create Contact Property with Loops

Creates a new contact property in Loops.

## Endpoint

- **Method:** `POST`
- **Path:** `/contacts/properties`
- **Base URL:** `https://app.loops.so/api/v1`
- **Official documentation:** [Create Contact Property](https://loops.so/docs/api-reference/create-contact-property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | — |
| `type` | body | `list` | yes | Accepted values: `boolean`, `date`, `number`, `string`. |
