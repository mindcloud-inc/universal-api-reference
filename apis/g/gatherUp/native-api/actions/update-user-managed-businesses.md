# Update User Managed Businesses with GatherUp

Updates a user's managed businesses in GatherUp.

## Endpoint

- **Method:** `POST`
- **Path:** `/user/update-managed-businesses`
- **Base URL:** `https://app.gatherup.com/api`
- **Official documentation:** [Update User Managed Businesses](https://app.gatherup.com/api/doc/user/update-managed-businesses)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `businessId{N}` | body | `number` | no | Managed business id. |
| `userId` | body | `number` | yes | Manager id. |
