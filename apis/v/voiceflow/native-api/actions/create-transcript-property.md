# Create Transcript Property with Voiceflow

Creates a new transcript property in Voiceflow.

## Endpoint

- **Method:** `POST`
- **Path:** `https://analytics-api.voiceflow.com/v1/transcript-property`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Create Transcript Property](https://docs.voiceflow.com/api-reference/transcript-property/create-transcript-property)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `name` | body | `string` | yes | The name of this property. |
| `type` | body | `string` | yes | The type of value held by this property. |
