# Create Radius List Count with PostcardMania

Creates a radius list count in PostcardMania.

## Endpoint

- **Method:** `POST`
- **Path:** `/list/count/radius`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Create Radius List Count](https://docs.pcmintegrations.com/docs/directmail-api/aafef87b8dd68-create-radius-list-count)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `breakdownType` | body | `string` | no | One of ZipCode, ZipCrrt, or Gender. |
| `demographics[]` | body | `array<object>` | no | Array of demographic filter objects. Use an empty array for no filters. |
| `listType` | body | `string` | no | PostcardMania list type key such as IRL. |
| `radius` | body | `object` | no | Radius object with radius, address, city, state, and zip. |
