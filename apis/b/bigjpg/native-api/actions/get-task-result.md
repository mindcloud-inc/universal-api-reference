# Get Task Result with Bigjpg

Retrieves task results from Bigjpg by task ID.

## Endpoint

- **Method:** `GET`
- **Path:** `/task/:taskIds`
- **Base URL:** `https://bigjpg.com/api`
- **Official documentation:** [Get Task Result](https://bigjpg.com/)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `taskIds` | path | `string` | yes | One or more Bigjpg task IDs, comma-separated in the request path. Send multiple values as a string separated by `,`. |
