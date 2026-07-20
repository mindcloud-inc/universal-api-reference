# Update Form Action with Form.io

Updates an existing form action in your Form.io project.

## Endpoint

- **Method:** `PUT`
- **Path:** `/form/:formId/action/:actionId`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Update Form Action](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID that owns the action. |
| `actionId` | path | `string` | yes | The form action ID. |
| `title` | body | `string` | yes | The action title. |
| `name` | body | `string` | yes | The action type name, such as save or role. |
| `handler[]` | body | `array<string>` | yes | One or more handler stages for the action. |
| `method[]` | body | `array<string>` | yes | One or more submission methods that trigger the action. |
| `priority` | body | `number` | no | The action priority. |
| `settings` | body | `object` | no | Action settings object. |
