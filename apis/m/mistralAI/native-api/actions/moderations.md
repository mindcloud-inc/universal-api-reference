# Moderations with Mistral AI

Creates text moderation results in Mistral AI.

## Endpoint

- **Method:** `POST`
- **Path:** `/v1/moderations`
- **Base URL:** `https://api.mistral.ai`
- **Official documentation:** [Moderations](https://docs.mistral.ai/api/endpoint/classifiers#operation-moderations_v1_moderations_post)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | body | `string` | yes | ID of the model to use. |
| `input[]` | body | `array<string>` | yes | Text inputs to moderate. |
| `metadata` | body | `object` | no | Optional metadata object for the request. |
