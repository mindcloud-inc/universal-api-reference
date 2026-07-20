# Get available extensions for image with Xata

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationID/extensions`
- **Base URL:** `https://api.xata.tech`
- **Official documentation:** [Get available extensions for image](https://xata.io/docs/api-reference/projects/get-available-extensions-for-image)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationID` | path | `string` | yes | Unique identifier of the organization to check instance type availability for |
| `image` | query | `string` | yes | Image for which we list extensions |
| `region` | query | `string` | no | Region to list extensions for image in |
