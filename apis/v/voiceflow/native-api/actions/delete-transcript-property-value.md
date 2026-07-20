# Delete Transcript Property Value with Voiceflow

Deletes a transcript property value from Voiceflow.

## Endpoint

- **Method:** `DELETE`
- **Path:** `https://analytics-api.voiceflow.com/v1/transcript-property-value/transcript/:transcriptId/property/:propertyId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Delete Transcript Property Value](https://docs.voiceflow.com/api-reference/transcript-property-value/delete-transcript-property-value)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `transcriptId` | path | `string` | yes | ID of the transcript to target. |
| `propertyId` | path | `string` | yes | ID of the property to target. |
