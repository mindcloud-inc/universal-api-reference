# Get Project Service Packages with Jetbuilt

Retrieve all of the service_packages attached to a given project.

## Endpoint

- **Method:** `GET`
- **Path:** `projects/:projectID/service_packages/[:servicePackageID]`
- **Base URL:** `https://app.jetbuilt.com/api/`
- **Official documentation:** [Get Project Service Packages](https://api.jetbuilt.com/customers?shell--json#get-all-service-packages-in-your-project)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `projectID` | path | `string` | yes |
| `servicePackageID` | path | `string` | no |
