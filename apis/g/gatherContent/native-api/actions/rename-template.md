# Rename Template with GatherContent

Renames an existing template in GatherContent.

## Endpoint

- **Method:** `POST`
- **Path:** `/templates/:template_id/rename`
- **Base URL:** `https://api.gathercontent.com`
- **Official documentation:** [Rename Template](https://docs.gathercontent.com/reference/renametemplate)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Template name. |
| `template_id` | path | `string` | yes | Template ID. |
