# Find Nearest Location with Data8

Finds the nearest location in Data8.

## Endpoint

- **Method:** `POST`
- **Path:** `/Location/FindMyNearest.json`
- **Base URL:** `https://webservices.data-8.co.uk`
- **Official documentation:** [Find Nearest Location](https://docs.data-8.co.uk/web-services/geocoding/findmynearest)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `licence` | body | `string` | yes | The licence type under which you are accessing the service. |
| `point` | body | `string` | yes | The coordinate point to search near. |
| `dataset` | body | `string` | no | The dataset to search within. |
| `options` | body | `object` | no | Optional settings that control location lookup behavior. |
