# Create Proposal In Project with Sunwise

Creates a new proposal in a Sunwise project.

## Endpoint

- **Method:** `POST`
- **Path:** `/proposals/:project_id/`
- **Base URL:** `https://production.sunwise.ai/boty/api/v1`
- **Official documentation:** [Create Proposal In Project](https://production.sunwise.ai/boty/docs)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `preset` | body | `string` | no | Optional preset name to seed the proposal |
| `project_id` | path | `string` | yes | Sunwise project identifier |
| `name` | body | `string` | yes | Proposal name |
