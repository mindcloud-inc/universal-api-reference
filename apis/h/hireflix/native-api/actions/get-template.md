# Get Template with Hireflix

Retrieves a template by type from Hireflix.

## Endpoint

- **Method:** `POST`
- **Path:** `me`
- **Base URL:** `https://api.hireflix.com`
- **Official documentation:** [Get Template](https://api.hireflix.com/me)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `variables.type` | body | `string` | yes | The Hireflix template type namespace. |
| `variables.id` | body | `string` | yes | The Hireflix template ID. |
