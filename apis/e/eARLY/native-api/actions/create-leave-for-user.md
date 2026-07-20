# Create Leave for User with EARLY

Creates a leave in EARLY for a user.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/v4/users/:userId/leaves`
- **Base URL:** `https://api.early.app`
- **Official documentation:** [Create Leave for User](https://developers.early.app/#1f769296-6d23-4a4e-b15a-401dd4e2dd30)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `userId` | path | `string` | yes | User ID. |
| `typeId` | body | `string` | yes | Leave type ID. |
| `startDate` | body | `string` | yes | Leave start timestamp. |
| `endDate` | body | `string` | yes | Leave end timestamp. |
| `note` | body | `string` | no | Optional leave note. |
