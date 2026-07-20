# Update Template Set with Bannerbear

Updates an existing template set in Bannerbear.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/template_sets/:uid`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Update Template Set](https://developers.bannerbear.com/v2/#update-a-template-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The unique ID of the template set to update. |
| `name` | body | `string` | no | A name for this template set. |
| `templates[]` | body | `array<string>` | yes | The complete updated list of template UIDs to keep in this template set. |
