# Create Form Action with Form.io

Creates a new form action in your Form.io project.

## Endpoint

- **Method:** `POST`
- **Path:** `/form/:formId/action`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Create Form Action](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID that will receive the action. |
| `title` | body | `string` | yes | The action title. |
| `name` | body | `string` | yes | The action type name, such as save or role. |
| `handler[]` | body | `array<string>` | yes | One or more handler stages for the action. |
| `method[]` | body | `array<string>` | yes | One or more submission methods that trigger the action. |
| `priority` | body | `number` | no | The action priority. |
| `settings` | body | `object` | no | Action settings object. |
