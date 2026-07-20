# Create Shared Setting with Insightful

Creates a new shared setting in Insightful.

## Endpoint

- **Method:** `POST`
- **Path:** `/shared-settings`
- **Base URL:** `https://app.insightful.io/api/v1`
- **Official documentation:** [Create Shared Setting](https://developers.insightful.io/#2f30e38e-b5b3-4788-a88d-58ce3d340d41)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `description` | body | `string` | no | A description for the shared settings. |
| `name` | body | `string` | yes | The shared settings name. |
| `settings` | body | `object` | yes | The shared settings payload object. |
| `type` | body | `string` | yes | The settings type. |
