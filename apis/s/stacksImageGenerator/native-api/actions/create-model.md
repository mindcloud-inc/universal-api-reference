# Create Model with 88stacks Image Generator

Creates a new image generation model in 88stacks Image Generator.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v1/models`
- **Base URL:** `https://api.88stacks.com`
- **Official documentation:** [Create Model](https://88stacks.com/docs/1.0/models/create.en.html)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | no | Name to assign to the model. |
| `description` | body | `string` | no | Description of the model. |
| `test` | body | `string` | no | Set this when you want to create a test model. |
| `training_link` | body | `string` | no | URL to a zip file of training images. |
| `prompts_link` | body | `string` | no | URL to a file containing prompts for training. |
| `images` | body | `list<string>` | no | One or more JPG images to upload directly for training. |
