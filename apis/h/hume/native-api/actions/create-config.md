# Create config with Hume

## Endpoint

- **Method:** `POST`
- **Path:** `/v0/evi/configs`
- **Base URL:** `https://api.hume.ai`
- **Official documentation:** [Create config](https://dev.hume.ai/reference/speech-to-speech-evi/configs/create-config)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | Config name. |
| `evi_version` | body | `string` | yes | EVI version to use. Supported values include 3 and 4-mini. |
| `voice` | body | `object` | yes | Voice reference object, for example {"provider":"HUME_AI","name":"Ava Song"}. |
| `version_description` | body | `string` | no | Optional config version description. |
