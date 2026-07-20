# Update Transcript Property with Voiceflow

Updates an existing transcript property in Voiceflow.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://analytics-api.voiceflow.com/v1/transcript-property/:propertyId`
- **Base URL:** `https://general-runtime.voiceflow.com`
- **Official documentation:** [Update Transcript Property](https://docs.voiceflow.com/api-reference/transcript-property/update-transcript-property)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `propertyId` | path | `string` | yes | ID of the property to target. |
| `name` | body | `string` | no | The name of this property. |
| `type` | body | `string` | no | The type of value held by this property. |
