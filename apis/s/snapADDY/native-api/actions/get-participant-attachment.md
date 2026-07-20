# Get Participant Attachment with snapADDY

## Endpoint

- **Method:** `GET`
- **Path:** `/visitreport/v1/attachment/:questionnaireId/:participantId/:attachmentId`
- **Base URL:** `https://api.snapaddy.com`
- **Official documentation:** [Get Participant Attachment](https://developers.snapaddy.com/visitreport-rest-api/reference/participant-attachment)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `questionnaireId` | path | `string` | yes | Questionnaire identifier |
| `participantId` | path | `string` | yes | Participant identifier |
| `attachmentId` | path | `string` | yes | Attachment identifier |
