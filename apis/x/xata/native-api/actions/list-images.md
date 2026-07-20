# Get available images with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/images`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Get available images](https://xata.io/docs/api-reference/projects/get-available-images)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization to check image availability |
| `region` | query | `string` | no | Region to check image availability for organization |
