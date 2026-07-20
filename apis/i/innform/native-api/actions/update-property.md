# Update Property with Innform

Updates an existing property in Innform.

## Endpoint

- **Method:** `PUT`
- **Path:** `/properties/{id}`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Update Property](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Updated property address. |
| `city` | body | `string` | no | Updated property city. |
| `country` | body | `string` | no | Updated property country. |
| `id` | path | `string` | yes | Property UUID. |
| `name` | body | `string` | no | Updated property name. |
