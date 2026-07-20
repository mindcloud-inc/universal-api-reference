# List Recently Accessed Documents with Nucleus One

Retrieves recently accessed documents from a Nucleus One organization.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/recentlyAccessedDocuments`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [List Recently Accessed Documents](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `cursor` | query | `string` | no | Pagination cursor |
