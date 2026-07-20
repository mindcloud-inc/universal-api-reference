# Create Client Response with Formbricks

Creates a new client response in Formbricks.

## Endpoint

- **Method:** `POST`
- **Path:** `/client/:environmentId/responses`
- **Base URL:** `https://app.formbricks.com/api/v2`
- **Official documentation:** [Create Client Response](https://formbricks.com/docs/api-v2-reference/client-api--response/create-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | path | `string` | yes | The environment ID that owns the survey. |
| `surveyId` | body | `string` | yes | The survey ID to submit the response to. |
| `finished` | body | `boolean` | yes | Whether the response is finished. |
| `data` | body | `object` | yes | Submitted response payload keyed by question IDs. |
