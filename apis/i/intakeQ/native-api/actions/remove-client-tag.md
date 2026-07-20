# Remove Client Tag with IntakeQ

Deletes a client tag assignment from IntakeQ.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/clientTags`
- **Base URL:** `https://intakeq.com/api/v1`
- **Official documentation:** [Remove Client Tag](https://support.intakeq.com/article/251-intakeq-client-api)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `clientId` | query | `string` | yes | The IntakeQ numeric client ID. |
| `tag` | query | `string` | yes | The client tag to remove. |
