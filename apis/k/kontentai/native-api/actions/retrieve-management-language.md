# Retrieve management language with Kontent.ai

Retrieves a language from your Kontent.ai environment.

## Endpoint

- **Method:** `GET`
- **Path:** `https://manage.kontent.ai/v2/projects/:environment_id/languages/:language_identifier`
- **Base URL:** `https://deliver.kontent.ai`
- **Official documentation:** [Retrieve management language](https://kontent.ai/learn/docs/apis/management-api-v2/languages)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `language_identifier` | path | `string` | yes | Kontent.ai language identifier. |
