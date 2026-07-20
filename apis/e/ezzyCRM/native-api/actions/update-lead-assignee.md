# Update Lead Assignee with EzzyCRM

## Endpoint

- **Method:** `POST`
- **Path:** `/api/assignlead`
- **Base URL:** `https://ezzycrm.com`
- **Official documentation:** [Update Lead Assignee](https://ezzycrm.com/api/PostApiDocument.aspx#assignlead)

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `DealId` | body | `number` | yes | ID of the lead. |
| `DealAssignUserId` | body | `number` | yes | ID of the assigned user. |
