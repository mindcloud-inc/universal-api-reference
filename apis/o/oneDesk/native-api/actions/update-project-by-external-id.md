# Update Project By External ID with OneDesk

Updates a project in OneDesk by external ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/rest/public/projects/externalId/:externalId`
- **Base URL:** `https://app.onedesk.com`
- **Official documentation:** [Update Project By External ID](https://onedesk.com/public-api/swagger.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `externalId` | path | `string` | yes | External ID of the project to update. |
| `name` | body | `string` | no | Updated name for the project. |
