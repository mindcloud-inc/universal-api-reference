# Create Template with Bannerbear

Creates a new template in Bannerbear.

## Endpoint

- **Method:** `POST`
- **Path:** `/v2/templates`
- **Base URL:** `https://api.bannerbear.com`
- **Official documentation:** [Create Template](https://developers.bannerbear.com/v2/#create-a-template)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of the new blank template. |
| `width` | body | `number` | yes | The width of the new blank template. |
| `height` | body | `number` | yes | The height of the new blank template. |
| `metadata` | body | `string` | no | Custom metadata to store with the template. |
| `tags[]` | body | `array<string>` | no | An array of tags for the template. |
