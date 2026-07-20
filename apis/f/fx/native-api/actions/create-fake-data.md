# Create Fake Data with 1001fx

Creates fake test data with 1001fx.

## Endpoint

- **Method:** `POST`
- **Path:** `/data/createfakedata`
- **Base URL:** `https://api.1001fx.com`
- **Official documentation:** [Create Fake Data](https://1001fx.com/functions/createfakedata)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `data[]` | body | `array` | yes | Array of fake-data definitions to generate. |
| `locale` | body | `string` | no | Locale used for generated fake data. |
| `rows` | body | `number` | no | Number of fake-data rows to generate. |
