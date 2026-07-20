# Update Application with Scaleway

Updates an existing application in Scaleway.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/iam/v1alpha1/applications/:application_id`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Update Application](https://www.scaleway.com/en/developers/api/iam/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `application_id` | path | `string` | yes |
| `name` | body | `string` | no |
