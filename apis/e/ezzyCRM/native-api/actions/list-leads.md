# List Leads with EzzyCRM

## Endpoint

- **Method:** `GET`
- **Path:** `/api/getallleads`
- **Base URL:** `https://ezzycrm.com`
- **Official documentation:** [List Leads](https://ezzycrm.com/api/GetApiDocument.aspx#getleads)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `PipelineId` | query | `number` | yes | Only leads within the given pipeline will be returned. |
| `UserId` | query | `number` | yes | Live testing showed this value must be supplied for the endpoint to resolve, even though the provider docs describe it as optional. |
| `FromDate` | query | `string` | yes | Only leads within the given date range will be returned. |
| `ToDate` | query | `string` | yes | Only leads within the given date range will be returned. |
