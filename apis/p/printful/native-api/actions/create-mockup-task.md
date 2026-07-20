# Create Mockup Task with Printful

Creates a mockup generation task in Printful.

## Endpoint

- **Method:** `POST`
- **Path:** `/mockup-generator/create-task/{id}`
- **Base URL:** `https://api.printful.com`
- **Official documentation:** [Create Mockup Task](https://developers.printful.com/docs/#tag/Mockup-Generator-API/operation/createGeneratorTask)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The Printful product variant id to generate mockups for. |
