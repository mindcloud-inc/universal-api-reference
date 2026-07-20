# Set Transcript Property Value with Voiceflow

Sets a transcript property value in Voiceflow.

## Endpoint

- **Method:** `POST`
- **Path:** `https://analytics-api.voiceflow.com/v1/transcript-property-value`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Set Transcript Property Value](https://docs.voiceflow.com/api-reference/transcript-property-value/set-transcript-property-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertyID` | body | `string` | yes | ID of the transcript property to target. |
| `transcriptID` | body | `string` | yes | ID of the transcript to target. |
| `value` | body | `string` | yes | Value of the transcript property to set. |
| `metadata` | body | `object` | no | Additional metadata associated with the property value. |
