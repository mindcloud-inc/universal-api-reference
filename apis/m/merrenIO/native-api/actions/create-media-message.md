# Create Media Message with MerrenIO

## Endpoint

- **Method:** `POST`
- **Path:** `/question/addMessage`
- **Base URL:** `https://app.merren.io`
- **Official documentation:** [Create Media Message](https://merren.io/api-integration/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `surveyId` | body | `string` | yes | Survey that will contain the message. |
| `sectionId` | body | `string` | yes | Section that will contain the message. |
| `message` | body | `string` | yes | Media caption or prompt for the message. |
