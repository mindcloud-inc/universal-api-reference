# Create Template Set with Bannerbear

Creates a new template set in Bannerbear.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/template_sets`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Create Template Set](https://developers.bannerbear.com/v2/#create-a-template-set)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | A name for this template set. |
| `templates[]` | body | `array<string>` | yes | A list of template UIDs to add to this template set. |
