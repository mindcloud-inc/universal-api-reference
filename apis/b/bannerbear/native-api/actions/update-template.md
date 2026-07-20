# Update Template with Bannerbear

Updates an existing template in Bannerbear.

## Endpoint

- **Method:** `PATCH`
- **Path:** `/v2/templates/:uid`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Update Template](https://developers.bannerbear.com/v2/#update-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `uid` | path | `string` | yes | The unique ID of the template to update. |
| `name` | body | `string` | no | The updated name of the template. |
| `metadata` | body | `string` | no | Custom metadata to store with the template. |
| `tags[]` | body | `array<string>` | no | An updated array of tags for the template. |
| `width` | body | `number` | no | The new width of the template. |
| `height` | body | `number` | no | The new height of the template. |
