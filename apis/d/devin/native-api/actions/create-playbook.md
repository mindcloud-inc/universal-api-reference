# Create Playbook with Devin

Creates a new playbook in Devin.

## Endpoint

- **Method:** `POST`
- **Path:** `/v3/organizations/:org_id/playbooks`
- **Base URL:** `https://api.devin.ai`
- **Official documentation:** [Create Playbook](https://docs.devin.ai/api-reference/v3/playbooks/post-organizations-playbooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `body` | body | `string` | yes | Playbook body/instructions. |
| `macro` | body | `string` | no | Optional playbook macro identifier such as !my_macro. |
| `org_id` | path | `string` | yes | Devin organization ID. |
| `title` | body | `string` | yes | Playbook title. |
