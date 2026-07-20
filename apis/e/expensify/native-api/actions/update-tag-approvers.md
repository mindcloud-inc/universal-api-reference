# Update Tag Approvers with Expensify

Updates tag approvers in Expensify.

## Endpoint

- **Method:** `POST`
- **Path:** `ExpensifyIntegrations`
- **Base URL:** `https://integrations.expensify.com/Integration-Server/`
- **Official documentation:** [Update Tag Approvers](https://integrations.expensify.com/Integration-Server/doc/#tag-approvers-updater)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `policyId` | body | `string` | yes | The Expensify policy ID to update. |
| `tagApproversJson` | body | `string` | yes | JSON array of tag approver assignments. |
