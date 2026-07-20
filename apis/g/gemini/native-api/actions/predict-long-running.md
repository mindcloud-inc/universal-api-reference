# Predict Long Running with Gemini

Starts a long-running prediction in Gemini.

## Endpoint

- **Method:** `POST`
- **Path:** `v1beta/models/:model`
- **Base URL:** `https://generativelanguage.googleapis.com`
- **Official documentation:** [Predict Long Running](https://ai.google.dev/api/models#v1beta.models.predictLongRunning)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `model` | path | `string` | yes | Required. Model endpoint token including suffix, for example veo-3.0-generate-001:predictLongRunning. |
| `instances[]` | body | `array<object>` | yes | Required prediction instances array. |
| `parameters` | body | `object` | no | Optional prediction parameters object. |
