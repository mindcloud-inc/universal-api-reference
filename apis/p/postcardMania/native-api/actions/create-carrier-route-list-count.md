# Create Carrier Route List Count with PostcardMania

Creates a carrier route list count in PostcardMania.

## Endpoint

- **Method:** `POST`
- **Path:** `/list/count/carrier-route`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Create Carrier Route List Count](https://docs.pcmintegrations.com/docs/directmail-api/65o0jh0i3n7in-generating-a-list-count-by-carrier-route)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `breakdownType` | body | `string` | no | One of ZipCode, ZipCrrt, or Gender. |
| `carrierRoutes[]` | body | `array<string>` | no | Array of carrier route strings like 33602:C001. |
| `demographics[]` | body | `array<object>` | no | Array of demographic filter objects. Use an empty array for no filters. |
| `listType` | body | `string` | no | PostcardMania list type key such as IRL. |
