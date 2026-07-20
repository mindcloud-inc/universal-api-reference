# Create Blank Datamodel with Sisense

Creates a blank datamodel in Sisense.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v2/datamodels`
- **Base URL:** `https://signup-126940n0.sisense.com`
- **Official documentation:** [Create Blank Datamodel](https://developer.sisense.com/guides/restApi/datamodels.v2.html#creating-a-blank-datamodel-object)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `title` | body | `string` | yes | Datamodel title. |
| `type` | body | `string` | no | Datamodel type. Use extract or live. |
