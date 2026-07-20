# Update Lead Tags with Leadboxer

Updates lead tags for a lead in Leadboxer.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v1/management/lead-tags`
- **Base URL:** `https://data.leadboxer.com`
- **Official documentation:** [Update Lead Tags](https://developers.leadboxer.com/reference/updateleadtags)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `datasetId` | body | `string` | yes |
| `leadId` | body | `string` | yes |
| `leadTags` | body | `string` | yes |
