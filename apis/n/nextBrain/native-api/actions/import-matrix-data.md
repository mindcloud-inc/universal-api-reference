# Import Matrix Data with NextBrain

Imports matrix data into a NextBrain dataset.

## Endpoint

- **Method:** `POST`
- **Path:** `/csv/import_matrix_token`
- **Base URL:** `https://api.nextbrain.ai`
- **Official documentation:** [Import Matrix Data](https://api.nextbrain.ai/docs)

## Headers

Send these additional headers for this operation:

| Header | Value |
| --- | --- |
| `Accept` | `application/json` |
| `Content-Type` | `application/json` |

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `matrix[]` | body | `array<array>` | yes | A matrix where the first row is the header and each following row is data. |
| `workspace_id` | body | `string` | no | Optional workspace or project ID for the import target. |
