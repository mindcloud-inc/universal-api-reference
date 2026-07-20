# Bulk Delete Rules with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/data-validation/rules/actions/bulk-delete`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Bulk Delete Rules](https://docs.kadoa.com/docs/ui/data-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `reason` | body | `string` | no | Reason for deletion |
| `ruleIds` | body | `string` | yes | JSON array of rule IDs |
| `workflowId` | body | `string` | yes | Workflow ID |
