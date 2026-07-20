# List Automations with MindMe

Retrieves automations from MindMe.

## Endpoint

- **Method:** `POST`
- **Path:** `/api/Automation/GetAutomationSummaryPagingWithFilter`
- **Base URL:** `https://prodapi.mindmemobile.com`
- **Official documentation:** [List Automations](https://prodapi.mindmemobile.com/swagger/v1/swagger.json#/paths/~1api~1Automation~1GetAutomationSummaryPagingWithFilter/post)

## Parameters

| Parameter | Location | Type | Required |
| --- | --- | --- | --- |
| `accountId` | body | `string` | no |
| `pageNumber` | body | `string` | no |
| `pageSize` | body | `string` | no |
| `userId` | body | `string` | no |
