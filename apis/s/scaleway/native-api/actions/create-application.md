# Create Application with Scaleway

Creates a new application in Scaleway.

## Endpoint

- **Method:** `POST`
- **Path:** `/iam/v1alpha1/applications`
- **Base URL:** `https://api.scaleway.com`
- **Official documentation:** [Create Application](https://www.scaleway.com/en/developers/api/iam/)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `name` | body | `string` | yes |
| `organization_id` | body | `string` | no |
