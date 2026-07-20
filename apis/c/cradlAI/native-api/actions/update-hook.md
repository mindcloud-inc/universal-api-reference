# Update Hook with Cradl AI

Updates an existing hook in Cradl AI.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/hooks/:hookId`
- **Base URL:** `https://api.cradl.ai/v1`
- **Official documentation:** [Update Hook](https://docs.cradl.ai/api-reference/patch-hooks)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `hookId` | path | `string` | yes | Identifier of the hook to update. |
| `name` | body | `string` | no | Updated hook name. |
| `description` | body | `string` | no | Updated hook description. |
| `trigger` | body | `list` | no | Updated trigger type for the hook. Accepted values: `ActionRun has Completed`, `Document is Created`, `Email is Received`, `Prediction is Created`, `ValidationTask has Completed`, `ValidationTask is Created`. |
| `enabled` | body | `boolean` | no | Whether the hook is enabled. |
| `functionId` | body | `string` | no | Updated function identifier used by the hook. |
| `trueActionId` | body | `string` | no | Updated action to run when the hook evaluates true. |
| `falseActionId` | body | `string` | no | Updated action to run when the hook evaluates false. |
| `config` | body | `object` | no | Updated hook configuration object. |
| `metadata` | body | `object` | no | Updated metadata attached to the hook. |
