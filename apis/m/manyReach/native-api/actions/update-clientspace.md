# Update Clientspace with ManyReach

Updates an existing clientspace in ManyReach.

## Endpoint

- **Method:** `PATCH`
- **Path:** `https://api.manyreach.com/api/v2/clientspaces/:id`
- **Base URL:** `https://api.manyreach.com`
- **Official documentation:** [Update Clientspace](https://api.manyreach.com/api#v2/tag/clientspace)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `autoAllocate` | body | `boolean` | no | Whether credits are allocated automatically. |
| `creditAmount` | body | `number` | no | Recurring credit amount for the clientspace. |
| `id` | path | `string` | yes | The ID of the clientspace to update. |
| `separateCredits` | body | `boolean` | no | Whether the clientspace uses a separate credit pool. |
| `title` | body | `string` | no | Clientspace display name. |
