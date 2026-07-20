# Create Leave for User with Timeular

Creates a leave request for a user in your Timeular workspace.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/users/:userId/leaves`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Leave for User](https://developers.early.app/#1f769296-6d23-4a4e-b15a-401dd4e2dd30)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `endDate` | body | `string` | yes |
| `note` | body | `string` | no |
| `startDate` | body | `string` | yes |
| `typeId` | body | `string` | yes |
| `userId` | path | `string` | yes |
