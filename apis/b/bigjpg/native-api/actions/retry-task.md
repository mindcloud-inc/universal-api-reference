# Retry Task with Bigjpg

Retries image enlargement tasks in Bigjpg by task ID.

## Endpoint

- **Method:** `POST`
- **Path:** `/task/:taskIds`
- **Base URL:** `https://bigjpg.com/api`
- **Official documentation:** [Retry Task](https://bigjpg.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskIds` | path | `string` | yes | One or more Bigjpg task IDs to retry, comma-separated in the request path. Send multiple values as a string separated by `,`. |
