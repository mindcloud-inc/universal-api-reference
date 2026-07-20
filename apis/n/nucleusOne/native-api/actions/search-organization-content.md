# Search Organization Content with Nucleus One

Finds organization content in Nucleus One by search query.

## Endpoint

- **Method:** `GET`
- **Path:** `/organizations/:organizationId/searchResults`
- **Base URL:** `https://client-api.nucleus.one/api/v1`
- **Official documentation:** [Search Organization Content](https://client-api.nucleus.one/api/v1/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `organizationId` | path | `string` | yes | ID of the organization |
| `cursor` | query | `string` | no | Pagination cursor |
