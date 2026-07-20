# Get what3words Grid Section with What3Words

Retrieves a what3words grid section by bounding box.

## Endpoint

- **Method:** `GET`
- **Path:** `/grid-section`
- **Base URL:** `https://api.what3words.com/v3`
- **Official documentation:** [Get what3words Grid Section](https://developer.what3words.com/public-api/docs#grid-section)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `bounding-box` | query | `string` | yes | Bounding box as south,west,north,east. The box must not exceed 4 km corner-to-corner. |
| `format` | query | `list<string>` | no | Response format: json or geojson. Accepted values: `geojson`, `json`. |
