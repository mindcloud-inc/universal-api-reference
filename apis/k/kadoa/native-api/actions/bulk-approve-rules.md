# Bulk Approve Rules with Kadoa

## Endpoint

- **Method:** `POST`
- **Path:** `/v4/data-validation/rules/actions/bulk-approve`
- **Base URL:** `https://api.kadoa.com`
- **Official documentation:** [Bulk Approve Rules](https://docs.kadoa.com/docs/ui/data-validation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ruleIds` | body | `string` | yes | JSON array of rule IDs |
| `workflowId` | body | `string` | yes | Workflow ID |
