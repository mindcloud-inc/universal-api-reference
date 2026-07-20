# Update Client Response with Formbricks

Updates an existing client response in Formbricks.

## Endpoint

- **Method:** `PUT`
- **Path:** `/client/:environmentId/responses/:responseId`
- **Base URL:** `https://app.formbricks.com/api/v2`
- **Official documentation:** [Update Client Response](https://formbricks.com/docs/api-v2-reference/client-api--response/update-response)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `environmentId` | path | `string` | yes | The environment ID that owns the survey response. |
| `responseId` | path | `string` | yes | The response ID to update. |
| `finished` | body | `boolean` | no | Whether the response is finished. |
| `data` | body | `object` | no | Updated response payload keyed by question IDs. |
