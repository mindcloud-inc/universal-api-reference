# Modify management language with Kontent.ai

Modifies a language in your Kontent.ai environment.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/languages/:language_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Modify management language](https://kontent.ai/learn/docs/apis/management-api-v2/languages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_identifier` | path | `string` | yes | Kontent.ai language identifier to modify. |
| `operations[]` | body | `array<object>` | yes | JSON Patch operations for modifying a Kontent.ai language. |
