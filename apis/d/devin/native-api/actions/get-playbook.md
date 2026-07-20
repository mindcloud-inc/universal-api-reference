# Get Playbook with Devin

Retrieves a playbook record from Devin.

## Endpoint

- **Method:** `GET`
- **Path:** `/v3/organizations/:org_id/playbooks/:playbook_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Get Playbook](https://docs.devin.ai/api-reference/v3/playbooks/get-organizations-playbooks-playbook-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `playbook_id` | path | `string` | yes | Playbook ID. |
