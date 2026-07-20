# Add Client Tag with IntakeQ

Creates a client tag assignment in IntakeQ.

## Endpoint

- **Method:** `POST`
- **Path:** `/clientTags`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Add Client Tag](https://support.intakeq.com/article/251-intakeq-client-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `ClientId` | body | `string` | yes | The IntakeQ numeric client ID. |
| `Tag` | body | `string` | yes | The client tag to add. |
