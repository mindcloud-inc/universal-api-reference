# Duplicate Form with Refiner

Creates a duplicate of a form in Refiner.

## Endpoint

- **Method:** `POST`
- **Path:** `/forms/duplicate`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Duplicate Form](https://refiner.io/docs/api/#duplicate-form)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `form_uuid` | body | `string` | yes | The source form UUID to duplicate. |
| `name` | body | `string` | yes | Name to assign to the duplicated draft form. |
