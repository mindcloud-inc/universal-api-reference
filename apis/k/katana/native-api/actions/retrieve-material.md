# Retrieve Material with Katana

Retrieves a material by ID from Katana.

## Endpoint

- **Method:** `GET`
- **Path:** `/materials/:id`
- **Base URL:** `https://api.katanamrp.com/v1`
- **Official documentation:** [Retrieve Material](https://developer.katanamrp.com/reference/getmaterial)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `number` | yes | Material id |
| `extend[]` | query | `array<string>` | no | Array of objects that need to be added to the response |
