# Tag Responses with Refiner

Updates tags on survey responses in Refiner.

## Endpoint

- **Method:** `POST`
- **Path:** `/responses/tags`
- **Base URL:** `https://api.refiner.io/v1`
- **Official documentation:** [Tag Responses](https://refiner.io/docs/api/#tag-responses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uuid` | body | `string` | yes | The Refiner survey response UUID to tag. |
| `tags[]` | body | `array<string>` | yes | Tags to add to the survey response. |
