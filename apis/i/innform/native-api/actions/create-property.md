# Create Property with Innform

Creates a new property in Innform.

## Endpoint

- **Method:** `POST`
- **Path:** `/properties`
- **Base URL:** `https://api.innform.io/v1`
- **Official documentation:** [Create Property](https://innform.docs.apiary.io/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `address` | body | `string` | no | Optional property address. |
| `city` | body | `string` | yes | Property city. |
| `country` | body | `string` | yes | Property country. |
| `name` | body | `string` | yes | Property name. |
