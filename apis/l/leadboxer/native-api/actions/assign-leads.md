# Assign Leads with Leadboxer

Assigns a lead to a user in Leadboxer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/management/assign-leads`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Assign Leads](https://developers.leadboxer.com/reference/assignleads)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `leadId` | body | `string` | yes |
| `datasetId` | body | `string` | yes |
| `assignee` | body | `number` | yes |
