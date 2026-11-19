# List Ticket Tags with Zoho Desk

This API searches for tags added in your help desk portal

## Endpoint

- **Method:** `GET`
- **Path:** `/ticketTags`
- **Base URL:** `https://desk.zoho.com/api/v1`
- **Official documentation:** [List Ticket Tags](https://desk.zoho.com/DeskAPIDocument#TicketTags#TicketTags_Listtickettags)

## Capabilities

This operation supports [pagination](../README.md#pagination).

## Parameters

| Parameter | Location | Type | Required | Description |
| --- | --- | --- | --- | --- |
| `departmentID` | query | `string` | yes | ID of the department from which the tags must be fetched. |
| `sortBy` | query | `string` | no | Key that sorts tags by a specific attribute: `createdTime` or `count`. The default sorting order is descending. |
