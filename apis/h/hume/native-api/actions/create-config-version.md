# Create config version with Hume

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/configs/:id`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create config version](https://dev.hume.ai/reference/speech-to-speech-evi/configs/create-config-version)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | EVI config identifier. |
| `evi_version` | body | `string` | yes | EVI version to use. Supported values include 3 and 4-mini. |
| `voice` | body | `object` | yes | Voice reference object, for example {"provider":"HUME_AI","name":"Ava Song"}. |
| `version_description` | body | `string` | no | Optional config version description. |
