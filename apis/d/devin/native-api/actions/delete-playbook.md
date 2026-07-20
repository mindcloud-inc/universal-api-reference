# Delete Playbook with Devin

Deletes an existing playbook from Devin.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/v3/organizations/:org_id/playbooks/:playbook_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Delete Playbook](https://docs.devin.ai/api-reference/v3/playbooks/delete-organizations-playbooks-playbook-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `playbook_id` | path | `string` | yes | Playbook ID. |
