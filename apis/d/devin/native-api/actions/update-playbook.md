# Update Playbook with Devin

Updates an existing playbook in Devin.

## Endpoint

- **Method:** `PUT`
- **Path:** `/v3/organizations/:org_id/playbooks/:playbook_id`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Update Playbook](https://docs.devin.ai/api-reference/v3/playbooks/put-organizations-playbooks-playbook-id)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Playbook body/instructions. |
| `macro` | body | `string` | no | Optional playbook macro identifier such as !my_macro. |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `playbook_id` | path | `string` | yes | Playbook ID. |
| `title` | body | `string` | yes | Playbook title. |
