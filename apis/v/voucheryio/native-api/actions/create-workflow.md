# Create Workflow with Vouchery.io

## Endpoint

- **Method:** `POST`
- **Path:** `/workflows`
- **Base URL:** `https://mindcloud.sandbox.vouchery.app/api/v2.1`
- **Official documentation:** [Create Workflow](https://docs.vouchery.io/reference/postapiv21workflows)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `type` | body | `string` | yes | Workflow type. Reactive or birthday. |
| `first_action_id` | body | `string` | yes | ID of the first workflow action. |
| `name` | body | `string` | yes | Workflow name. |
| `actions[]` | body | `array<object>` | yes | Workflow action graph. |
| `metadata` | body | `object` | yes | Workflow metadata object. |
| `expires_in` | body | `string` | yes | Workflow expiry duration string. |
| `namespace` | body | `string` | no | Workflow namespace. |
| `before_birthday` | body | `number` | no | Days before birthday for birthday workflows. |
| `launch_criteria` | body | `object` | no | Launch criteria filter definition. |
| `valid_from` | body | `string` | no | Workflow validity start. |
| `valid_to` | body | `string` | no | Workflow validity end. |
