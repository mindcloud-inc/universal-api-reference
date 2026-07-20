# Remove Loop Member with HITL Platform

## Endpoint

- **Method:** `DELETE`
- **Path:** `/api/loops/:id/members/:userId`
- **Base URL:** `https://api.hitl.sh/v1`
- **Official documentation:** [Remove Loop Member](https://docs.hitl.sh/api-reference/introduction)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `id` | path | `string` | yes | The unique identifier of the loop. |
| `userId` | path | `string` | yes | The unique identifier of the loop member to remove. |
