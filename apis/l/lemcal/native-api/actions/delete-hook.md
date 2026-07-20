# Delete Hook with Lemcal

Deletes an existing hook from Lemcal.

## Endpoint

- **Method:** `DELETE`
- **Path:** `/hooks/:id`
- **Base URL:** `https://api.lemcal.com/api/lemcal`
- **Official documentation:** [Delete Hook](https://developer.lemcal.com/#delete-a-hook)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The ID of the hook to delete. |
