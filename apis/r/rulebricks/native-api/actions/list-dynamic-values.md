# List Dynamic Values with Rulebricks

Retrieves dynamic values from Rulebricks.

## Endpoint

- **Method:** `GET`
- **Path:** `/values`
- **Base URL:** `https://rulebricks.com/api/v1`
- **Official documentation:** [List Dynamic Values](https://rulebricks.com/docs/api-reference)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `include` | query | `string` | no | Additional data to include, such as usage |
| `name` | query | `string` | no | Query values containing a specific name |
