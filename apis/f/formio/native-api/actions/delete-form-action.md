# Delete Form Action with Form.io

Deletes an existing form action from your Form.io project.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/form/:formId/action/:actionId`
- **Base URL:** `https://neabnzbnvbushtk.form.io`
- **Official documentation:** [Delete Form Action](https://help.form.io/developers/introduction/api-documentation)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `formId` | path | `string` | yes | The form ID that owns the action. |
| `actionId` | path | `string` | yes | The form action ID to delete. |
