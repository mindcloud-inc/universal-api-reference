# Create Zipcode List Count with PostcardMania

Creates a ZIP code list count in PostcardMania.

## Endpoint

- **Method:** `POST`
- **Path:** `/list/count/zipcode`
- **Base URL:** `https://v3.pcmintegrations.com`
- **Official documentation:** [Create Zipcode List Count](https://docs.pcmintegrations.com/docs/directmail-api/42360cfbf8ceb)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `breakdownType` | body | `string` | no | One of ZipCode, ZipCrrt, or Gender. |
| `demographics[]` | body | `array<object>` | no | Array of demographic filter objects. Use an empty array for no filters. |
| `listType` | body | `string` | no | PostcardMania list type key such as IRL. |
| `zipCodes[]` | body | `array<string>` | no | Array of ZIP code strings. |
