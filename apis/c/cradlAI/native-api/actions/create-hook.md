# Create Hook with Cradl AI

Creates a new hook in Cradl AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/hooks`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Create Hook](https://docs.cradl.ai/api-reference/post-hooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Hook name. |
| `description` | body | `string` | no | Hook description. |
| `trigger` | body | `list` | no | Trigger type for the hook. Accepted values: `ActionRun has Completed`, `Document is Created`, `Email is Received`, `Prediction is Created`, `ValidationTask has Completed`, `ValidationTask is Created`. |
| `enabled` | body | `boolean` | no | Whether the hook is enabled. |
| `functionId` | body | `string` | no | Function identifier used by the hook. |
| `trueActionId` | body | `string` | no | Action to run when the hook evaluates true. |
| `falseActionId` | body | `string` | no | Action to run when the hook evaluates false. |
| `config` | body | `object` | no | Hook configuration object. |
| `metadata` | body | `object` | no | Metadata attached to the hook. |
