# Update Agent with PromptLayer Run Agent

Updates an existing workflow in PromptLayer.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/rest/workflows/:workflow_id_or_name`
- **Base URL:** `https://api.promptlayer.com`
- **Official documentation:** [Update Agent](https://docs.promptlayer.com/reference/patch-workflow)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `workflow_id_or_name` | path | `string` | yes | The PromptLayer agent ID or name to update. |
| `base_version` | body | `number` | no | Optional version number to base the patch on. |
| `commit_message` | body | `string` | no | A message describing the update. |
| `nodes` | body | `object` | yes | Partial node updates keyed by existing or new node name. |
| `required_input_variables` | body | `object` | no | Optional required input variable contract for the updated agent version. |
| `edges[]` | body | `array<object>` | no | Optional full edge list to store on the new agent version. |
| `release_labels[]` | body | `array<string>` | no | Optional release labels to attach to the new agent version. |
